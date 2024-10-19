# AWS EC2 Windows Server 2022 mit dynamisch hinzugefügtem EBS Volume

## Ziel der Übung
Ich habe eine EC2-Instanz mit Windows Server 2022 erstellt und ein zusätzliches EBS-Volume dynamisch hinzugefügt. Dieses Volume habe ich formatiert und als Laufwerk D: genutzt.

---

## Schritte

1. **EC2-Instanz erstellen**:  
   Ich habe eine **Windows Server 2022 Base Instanz** mit dem Typ **t2.micro** über die AWS Management Console gestartet und ein bestehendes **Key-Pair** verwendet.

   *Bild von der Erstellung der Instanz einfügen*

2. **Inbound-Rule für RDP hinzufügen**:  
   Ich habe in der **Security Group** eine **Inbound-Regel** für **RDP (Port 3389)** hinzugefügt.

   *Bild der hinzugefügten Inbound-Rule einfügen*

3. **RDP-Verbindung zur Instanz**:  
   Ich habe eine **RDP-Verbindung** zur Instanz aufgebaut, indem ich den **Public DNS Name**, **Username** (Administrator) und das entschlüsselte **Password** verwendet habe.

   *Bild der RDP-Verbindung einfügen*

4. **EBS-Volume erstellen und anhängen**:  
   Ich habe ein neues **EBS-Volume** mit **20 GB** erstellt und an die laufende Instanz angehängt.

   *Bild des erstellten und angehängten Volumes einfügen*

5. **Volume initialisieren und formatieren**:  
   In der **Laufwerksverwaltung** habe ich das Volume **online** geschaltet, **initialisiert** und als **einfaches Volume** mit dem Laufwerksbuchstaben **D:** formatiert.

   *Bild der Initialisierung und Formatierung des Volumes einfügen*

6. **Verzeichnis erstellen**:  
   Auf Laufwerk **D:** habe ich einen Ordner mit dem Namen **M346_MeinNachname** erstellt.

   *Bild des erstellten Verzeichnisses auf Laufwerk D: einfügen*

---

## Fazit
Ich habe gelernt, wie man dynamisch ein EBS-Volume zu einer EC2-Instanz hinzufügt und es im Betriebssystem formatiert und nutzt.
