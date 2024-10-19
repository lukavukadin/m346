# AWS EC2 Windows Server 2022 mit dynamisch hinzugefügtem EBS Volume

## Ziel der Übung
Ich habe eine EC2-Instanz mit Windows Server 2022 erstellt und ein zusätzliches EBS-Volume dynamisch hinzugefügt. Dieses Volume habe ich formatiert und als Laufwerk D: genutzt.

---

## Schritte

1. **EC2-Instanz erstellen**:  
   Ich habe eine **Windows Server 2022 Base Instanz** mit dem Typ **t2.micro** über die AWS Management Console gestartet und ein bestehendes **Key-Pair** verwendet.

2. **Inbound-Rule für RDP hinzufügen**:  
   Ich habe in der **Security Group** eine **Inbound-Regel** für **RDP (Port 3389)** hinzugefügt.

   <img src="https://github.com/user-attachments/assets/846cef74-f5ca-4d29-bee5-7959babdcdf5" alt="Inbound Rule" width="80%">

3. **RDP-Verbindung zur Instanz**:  
   Ich habe eine **RDP-Verbindung** zur Instanz aufgebaut, indem ich den **Public DNS Name**, **Username** (Administrator) und das entschlüsselte **Password** verwendet habe.

   <img src="https://github.com/user-attachments/assets/270332e2-2569-4a8e-86ea-9e6de5e52bd8" alt="RDP Verbindung" width="80%">
   <img src="https://github.com/user-attachments/assets/e2b25ea4-feaf-4254-9dfb-1b4d777a8756" alt="RDP Verbindung" width="80%">

4. **Überprüfung der Availability Zone**:  
   Bevor ich das EBS-Volume erstellt habe, habe ich überprüft, in welcher **Availability Zone** meine Instanz läuft, um sicherzustellen, dass das Volume in derselben Zone erstellt wird.

![image](https://github.com/user-attachments/assets/6cddee5a-8542-4824-9da7-9947ca96d640)


5. **EBS-Volume erstellen und anhängen**:  
   Ich habe ein neues **EBS-Volume** mit **20 GB** erstellt und an die laufende Instanz angehängt.

   <img src="https://github.com/user-attachments/assets/499bab7a-772b-43f4-9e23-a111592b8309" alt="EBS Volume erstellen" width="80%">
   <img src="https://github.com/user-attachments/assets/2ec97609-68b4-48f6-bff3-f029343c4db0" alt="EBS Volume anhängen" width="80%">

6. **Volume initialisieren und formatieren**:  
   In der **Laufwerksverwaltung** habe ich das Volume **online** geschaltet, **initialisiert** und als **einfaches Volume** mit dem Laufwerksbuchstaben **D:** formatiert.

   <img src="https://github.com/user-attachments/assets/36f27528-1464-432d-b81e-1045b5057b44" alt="Volume initialisieren" width="80%">

7. **Verzeichnis erstellen**:  
   Auf Laufwerk **D:** habe ich einen Ordner mit dem Namen **M346_MeinNachname** erstellt.

   <img src="https://github.com/user-attachments/assets/819037cd-563f-417e-9862-d1032c934a80" alt="Verzeichnis erstellen" width="80%">

---

## Fazit
Ich habe gelernt, wie man dynamisch ein EBS-Volume zu einer EC2-Instanz hinzufügt und es im Betriebssystem formatiert und nutzt.
