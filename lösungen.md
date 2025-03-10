# Praktischer Test Anleitung

## 1. Grundkonfiguration der Firewall (5 Punkte | Richtzeit 8 Minuten)

### Schritt-für-Schritt-Anleitung:

1.  **Webinterface öffnen:**
    *   Öffne deinen Webbrowser und gib die Standard-IP-Adresse der Firewall ein (falls nicht anders angegeben).
2.  **Anmelden:**
    *   Melde dich mit den Standard-Zugangsdaten an (falls nicht geändert: Benutzername `root`, Passwort `opnsense`).
3.  **Hostname ändern:**
    *   Gehe zu `System` → `Settings` → `General`.
    *   Trage unter `Hostname` den Wert `fwzh.skynet.local` ein.
4.  **Zeitzone einstellen:**
    *   Wähle unter `Timezone` den Eintrag `Europe/Zurich` aus.
5.  **Netzwerkadapter konfigurieren:**
    *   Gehe zu `Interfaces` → `WAN`.
    *   Stelle sicher, dass der WAN-Adapter auf `DHCP` eingestellt ist.
    *   Gehe zu `Interfaces` → `LAN`.
    *   Trage unter `IPv4 Configuration Type` den Wert `Static IPv4` ein.
    *   Trage unter `IPv4 Address` den Wert `172.16.0.1/24` ein.
    *   Gehe zu `Interfaces` und erstelle eine neue Schnittstelle für die DMZ.
    *   Wähle als `IPv4 Configuration Type` den Wert `Static IPv4`.
    *   Trage unter `IPv4 Address` den Wert `95.120.45.97/29` ein.
6.  **DHCP-Server aktivieren und konfigurieren:**
    *   Gehe zu `Services` → `DHCPv4` → `LAN`.
    *   Aktiviere den DHCP-Server, indem du ein Häkchen bei `Enable DHCP server on LAN interface` setzt.
    *   Trage unter `Range start` den Wert `172.16.0.100` ein.
    *   Trage unter `Range end` den Wert `172.16.0.200` ein.
7.  **Webinterface-Zugriff auf HTTPS beschränken:**
    *   Gehe zu `System` → `Settings` → `Administration`.
    *   Wähle unter `Protocol` den Eintrag `HTTPS` aus.
    *   Deaktiviere `HTTP redirect`.
8.  **Speichern und Anwenden:**
    *   Klicke auf `Save` und dann auf `Apply changes`, um die Änderungen zu übernehmen.

### Parameter-Tabelle

| Parameter            | Wert                     |
| :------------------- | :----------------------- |
| Hostname             | fwzh.skynet.local        |
| Zeitzone             | Europe/Zurich            |
| Netzwerkadapter 1    | WAN, DHCP                |
| Netzwerkadapter 2    | LAN, 172.16.0.1/24       |
| Netzwerkadapter 3    | DMZ, 95.120.45.97/29      |
| LAN Netzwerk         | DHCP Server aktiv Range: 172.16.0.100 - 172.16.0.200 |
| Zugriff Webinterface | Nur HTTPS (HTTP deaktiviert) |

## 2. Firewallregeln (8 Punkte | Richtzeit 10 Minuten)

### Schritt-für-Schritt-Anleitung:

1.  **Firewallregeln öffnen:**
    *   Gehe zu `Firewall` → `Rules` → `LAN`.
2.  **Regeln erstellen:**
    *   Erstelle die folgenden Regeln, indem du auf das `+` Symbol klickst:
        *   **Regel für LAN → ANY:**
            *   `Action`: `Pass`
            *   `Interface`: `LAN`
            *   `Protocol`: `Any`
            *   `Source`: `LAN net`
            *   `Destination`: `Any`
            *   Klicke auf `Save`.
        *   **Regel für DMZ → !LAN:**
            *   `Action`: `Pass`
            *   `Interface`: `DMZ`
            *   `Protocol`: `Any`
            *   `Source`: `DMZ net`
            *   `Destination`: `LAN net` (invertiere die Auswahl mit `!`)
            *   Klicke auf `Save`.
        *   **Regel für ANY → udp/5060:**
            *   `Action`: `Pass`
            *   `Interface`: `WAN`
            *   `Protocol`: `UDP`
            *   `Source`: `Any`
            *   `Destination`: `This Firewall`
            *   `Destination port range`: `5060`
            *   Klicke auf `Save`.
        *   **Regel für ANY → tcp/25:**
            *   `Action`: `Pass`
            *   `Interface`: `WAN`
            *   `Protocol`: `TCP`
            *   `Source`: `Any`
            *   `Destination`: `This Firewall`
            *   `Destination port range`: `25`
            *   Klicke auf `Save`.
        *   **Regel für ANY → tcp/80, tcp/443:**
            *   `Action`: `Pass`
            *   `Interface`: `WAN`
            *   `Protocol`: `TCP`
            *   `Source`: `Any`
            *   `Destination`: `This Firewall`
            *   `Destination port range`: `80, 443`
            *   Klicke auf `Save`.
        *   **Regel für ANY → icmp/8:**
            *   `Action`: `Pass`
            *   `Interface`: `WAN`
            *   `Protocol`: `ICMP`
            *   `ICMP subtype`: `Echo Request`
            *   `Source`: `Any`
            *   `Destination`: `This Firewall`
            *   Klicke auf `Save`.
        *   **Regel für syscomnet → tcp/3389:**
            *   Erstelle Alias für `syscomnet`. Gehe zu `Firewall` → `Aliases` und erstelle ein neues Alias mit dem Namen `syscomnet` und trage die IP-Adressen der Syscomnet AG ein.
            *   `Action`: `Pass`
            *   `Interface`: `WAN`
            *   `Protocol`: `TCP`
            *   `Source`: `syscomnet` (wähle das erstellte Alias)
            *   `Destination`: `This Firewall`
            *   `Destination port range`: `3389`
            *   Klicke auf `Save`.
3.  **Regeln anwenden:**
    *   Klicke auf `Apply changes`, um die Änderungen zu übernehmen.

### Port-Matrix

|           | srvwin    | srvvoip   | srvmail   | srvwww    | syscomnet | LAN   | DMZ     | ANY             |
| :-------- | :-------- | :-------- | :-------- | :-------- | :-------- | :---- | :------ | :-------------- |
| srvwin    |           |           |           |           |           |       |         |                 |
| srvvoip   |           |           |           |           |           |       |         |                 |
| srvmail   |           |           |           |           |           |       |         |                 |
| srvwww    |           |           |           |           |           |       |         |                 |
| syscomnet |           |           |           |           |           |       |         | tcp/3389        |
| LAN       | ANY       |           |           |           |           |       |         |                 |
| DMZ       | !LAN      |           |           |           |           |       |         |                 |
| ANY       | udp/5060  | tcp/25    | tcp/80    | tcp/443   | icmp/8    |       |         |                 |

## 3. Port-Weiterleitung (3 Punkte | Richtzeit 5 Minuten)

### Schritt-für-Schritt-Anleitung:

1.  **Port-Weiterleitung öffnen:**
    *   Gehe zu `Firewall` → `NAT` → `Port Forward`.
2.  **Neue Regel erstellen:**
    *   Klicke auf das `+` Symbol, um eine neue Regel zu erstellen.
    *   `Interface`: `WAN`
    *   `Protocol`: `TCP`
    *   `Source`: `Single host or alias` und wähle das Alias `syscomnet` aus.
    *   `Destination`: `WAN address`
    *   `Destination port range`: `3388`
    *   `Redirect target IP`: Gib die IP-Adresse des Servers `srvwin` ein (z.B. `172.16.0.x`).
    *   `Redirect target port`: `3389`
    *   `Description`: `Forward RDP to srvwin`
    *   Klicke auf `Save`.
3.  **Regeln anwenden:**
    *   Klicke auf `Apply changes`, um die Änderungen zu übernehmen.

## 4. Certificate Authority (7 Punkte | Richtzeit 5 Minuten)

### Schritt-für-Schritt-Anleitung:

1.  **CA-Manager öffnen:**
    *   Gehe zu `System` → `Certificates` → `Authorities`.
2.  **Neue CA erstellen:**
    *   Klicke auf das `+` Symbol, um eine neue CA zu erstellen.
    *   `Method`: `Create an internal Certificate Authority`
    *   `Descriptive name`: `Alphaone CA`
    *   `Key length`: `4096`
    *   `Digest Algorithm`: `SHA512`
    *   `Lifetime`: `3650`
    *   `Country Code`: `CH`
    *   `State or Province`: `ZH`
    *   `City`: `Zürich`
    *   `Organization`: `Alphaone AG`
    *   `Email Address`: `tech@alphaone.com`
    *   `Common Name`: `alphaone-ca`
    *   Klicke auf `Save`.

### Parameter-Tabelle

| Parameter       | Wert              |
| :-------------- | :---------------- |
| Descriptive Name | Alphaone CA       |
| Country Code    | CH                |
| State           | ZH                |
| City            | Zürich            |
| Organization    | Alphaone AG       |
| Email Address   | tech@alphaone.com |
| Common Name     | alphaone-ca       |

## 5. Remote-Access mit VPN (13 Punkte / Richtzeit 13 Minuten)

### 5.1 OpenVPN Server Zertifikat (4 Punkte | 5 Minuten)

### Schritt-für-Schritt-Anleitung:

1.  **Zertifikate öffnen:**
    *   Gehe zu `System` → `Certificates` → `Certificates`.
2.  **Neues Zertifikat erstellen:**
    *   Klicke auf das `+` Symbol, um ein neues Zertifikat zu erstellen.
    *   `Method`: `Create an internal Certificate`
    *   `Descriptive name`: `OpenVPN Server`
    *   `Certificate authority`: `Alphaone CA` (die zuvor erstellte CA auswählen)
    *   `Key length`: `4096`
    *   `Digest Algorithm`: `SHA512`
    *   `Lifetime`: `3650`
    *   `Common Name`: `fwzh`
    *   `Alternative names`: `80.234.92.105`
    *   Klicke auf `Save`.

### Parameter-Tabelle

| Parameter       | Wert             |
| :-------------- | :--------------- |
| Descriptive Name | OpenVPN Server   |
| Lifetime        | 3650             |
| Common Name     | fwzh             |
| IP-Adresse      | 80.234.92.105    |

### 5.2 VPN Einstellungen (6 Punkte | 5 Minuten)

### Schritt-für-Schritt-Anleitung:

1.  **OpenVPN Server öffnen:**
    *   Gehe zu `VPN` → `OpenVPN` → `Servers`.
2.  **Neuen Server erstellen:**
    *   Klicke auf das `+` Symbol, um einen neuen Server zu erstellen.
    *   `Description`: `OpenVPN Server`
    *   `Interface`: `WAN`
    *   `Protocol`: `TCP`
    *   `Device mode`: `SSL/TLS + User Auth`
    *   `IPv4 Tunnel Network`: Wähle einen nicht verwendeten IP-Adressbereich (z.B. `10.0.8.0/24`).
    *   `IPv4 Local Network`: `172.16.0.0/24` (dein LAN-Netzwerk)
    *   `Port`: `1194`
    *   `TLS Authentication`: Aktiviere diese Option.
    *   `Encryption algorithm`: `AES-256-GCM`
    *   `Auth Digest Algorithm`: `SHA512`
    *   `Certificate`: Wähle das zuvor erstellte Zertifikat `OpenVPN Server` aus.
    *   `Certificate Authority`: `Alphaone CA`
    *   `Strict User-CN Matching`: Deaktivieren
    *   Klicke auf `Save`.
3.  **Firewall-Regel für OpenVPN erstellen:**
    *   Gehe zu `Firewall` → `Rules` → `OpenVPN`.
    *   Erstelle eine neue Regel, um den OpenVPN-Traffic zu erlauben:
        *   `Action`: `Pass`
        *   `Interface`: `OpenVPN`
        *   `Protocol`: `Any`
        *   `Source`: `OpenVPN net`
        *   `Destination`: `LAN net`
        *   Klicke auf `Save`.
    *   Klicke auf `Apply changes`.

### Parameter-Tabelle

| Parameter                   | Wert                                                                                       |
| :-------------------------- | :----------------------------------------------------------------------------------------- |
| Transport Protokoll und Port | TCP/1194                                                                                   |
| Verschlüsselungsalgorithmus  | AES                                                                                        |
| Schlüssellänge              | 256 Bit                                                                                    |
| Block Chaining              | GCM                                                                                        |
| Hashing-Algorithmus         | SHA                                                                                        |
| Hash-Länge                  | 256 Bit                                                                                    |

### 5.3 Client Export (3 Punkte | 5 Minuten)

### Schritt-für-Schritt-Anleitung:

1.  **Benutzer erstellen:**
    *   Gehe zu `System` → `Access` → `Users`.
    *   Klicke auf das `+` Symbol, um einen neuen Benutzer zu erstellen.
    *   `Username`: `John`
    *   `Password`: Wähle ein sicheres Passwort.
    *   `Full name`: `John Doe`
    *   `Certificate`: `Create a new certificate for this user`
        *   `Method`: `Create an internal Certificate`
        *   `Certificate authority`: `Alphaone CA` (die zuvor erstellte CA auswählen)
        *   `Key length`: `4096`
        *   `Digest Algorithm`: `SHA512`
        *   `Lifetime`: `3650`
        *   `Common Name`: `John Doe`
    *   Klicke auf `Save`.
2.  **Client-Konfiguration exportieren:**
    *   Gehe zu `VPN` → `OpenVPN` → `Client Export`.
    *   Wähle unter `User` den Benutzer `John` aus.
    *   Wähle unter `Export type` den Eintrag `Viscosity (*.visz)` aus.
    *   Klicke auf `Download`.
    *   Speichere die Datei `John.visz` im Lösungsordner auf deiner Prüfungsdisk.

### Parameter-Tabelle

| Parameter       | Wert              |
| :-------------- | :---------------- |
| Username        | John              |
| Name            | John Doe          |
| OpenVPN Client  | Viscosity (\*.visz) |

## 6. Webzertifikat der Firewall (4 Punkte | Richtzeit 4 Minuten)

### Schritt-für-Schritt-Anleitung:

1.  **Zertifikate öffnen:**
    *   Gehe zu `System` → `Certificates` → `Certificates`.
2.  **Neues Zertifikat erstellen:**
    *   Klicke auf das `+` Symbol, um ein neues Zertifikat zu erstellen.
    *   `Method`: `Create an internal Certificate`
    *   `Descriptive name`: `OPNsense Web`
    *   `Certificate authority`: `Alphaone CA` (die zuvor erstellte CA auswählen)
    *   `Key length`: `4096`
    *   `Digest Algorithm`: `SHA512`
    *   `Lifetime`: `3650`
    *   `Common Name`: `fwzh`
    *   `Alternative names`: `172.16.0.1`
    *   Klicke auf `Save`.
3.  **Webinterface-Zertifikat aktivieren:**
    *   Gehe zu `System` → `Settings` → `Administration`.
    *   Wähle unter `SSL Certificate` das Zertifikat `OPNsense Web` aus.
    *   Klicke auf `Save`.
    *   Klicke auf `Apply changes`.

### Parameter-Tabelle

| Parameter       | Wert            |
| :-------------- | :-------------- |
| Descriptive Name | OPNsense Web    |
| Lifetime        | 3650            |
| Common Name     | fwzh            |
| IP-Adresse      | 172.16.0.1      |

## 7. Prüfungsabgabe

### Schritt-für-Schritt-Anleitung:

1.  **Konfigurations-Backup erstellen:**
    *   Gehe zu `System` → `Configuration` → `Backups`.
    *   Stelle sicher, dass `Encrypt configuration` nicht aktiviert ist.
    *   Stelle sicher, dass `Include RRD data` nicht aktiviert ist.
    *   Klicke auf `Download configuration`.
    *   Speichere die XML-Datei im Lösungsordner auf deiner Prüfungsdisk.

### 7.1 Inhalt des Lösungsordners

*   `John.visz` (OpenVPN-Konfiguration des Benutzers John)
*   `config.xml` (oder ähnlich, die Konfigurationsdatei im XML-Format)
