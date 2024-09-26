# Webserver und Datenbank Setup auf EC2

## 1. SSH-Zugang
Zuerst habe ich mich mit dem SSH-Key verbunden:

![SSH-Zugang](https://github.com/user-attachments/assets/863f0d32-bfa5-4e51-9e10-6bc7c10a5991)

## 2. Systemupdate
Dann habe ich das System mit folgendem Befehl aktualisiert:

![Systemupdate](https://github.com/user-attachments/assets/062cf5a0-92ff-4b72-b079-197b44307a0e)

## 3. Apache Installation
Hier wird der Apache Webserver installiert:

![Apache Installation](https://github.com/user-attachments/assets/d61fee38-4526-43c0-95ec-711f07d432e5)

## 4. PHP Installation
Das folgende Bild zeigt die Installation von PHP:

![PHP Installation](https://github.com/user-attachments/assets/8d6bfcc2-a6c4-4f99-9915-bc251f8212fa)

## 5. Apache und PHP Verbindung
Hier wird die Verbindung zwischen Apache und PHP installiert:

![Apache PHP Verbindung](https://github.com/user-attachments/assets/2e3cda67-27bb-4298-8932-33be685838ea)

## 6. MariaDB Server Installation
Nun installiere ich den MariaDB Server:

![MariaDB Installation](https://github.com/user-attachments/assets/0b219b0f-0fff-4eb6-a88b-b0aba574591d)

## 7. Serverstatus
Ich habe die Server neu gestartet und den Status überprüft:

![Serverstatus](https://github.com/user-attachments/assets/07d3a517-b84d-4e7a-8648-12b33ccce152)

## Webzugriff überprüfen

### 1. Apache Webserver
**Die folgende Abbildung zeigt die Standard-Startseite des Apache Webservers. Dies bestätigt, dass der Apache Webserver erfolgreich installiert und ausgeführt wird.**

![Apache Webserver](https://github.com/user-attachments/assets/aa776bc5-5a92-4228-a891-f8695f889c24)

### 2. PHP Info
**Hier ist die PHP-Informationsseite, die zeigt, dass PHP korrekt installiert ist und funktioniert. Diese Seite enthält wichtige Details über die PHP-Konfiguration und die installierten Module.**

![PHP Info](https://github.com/user-attachments/assets/e4140f06-aa7e-4943-9bb2-8c14a64db3dc)

### 3. Datenbankverbindung
**Diese Abbildung zeigt die Seite zur Datenbankverbindung. Wenn diese Seite erfolgreich geladen wird, bestätigt dies, dass die Verbindung zur MariaDB-Datenbank funktioniert.**

![Datenbankverbindung](https://github.com/user-attachments/assets/a3fdb43d-5af6-4b8f-b4da-b830ff917d96)
