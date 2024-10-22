# VPC erstellen und Webserver darin deployen

## Was ist eine VPC?

Eine Virtual Private Cloud (VPC) ist ein privates Netzwerk in der Cloud, das man vollständig kontrollieren kann. Es ermöglicht die Bereitstellung und Verwaltung von Servern oder anderen Ressourcen innerhalb eines isolierten Netzwerks.

## 1. VPC erstellen

Zuerst habe ich eine neue VPC erstellt mit der einstellung, in der ich später den Webserver betreiben werde.

### Screenshot: VPC Workflow erstellen

![image](https://github.com/user-attachments/assets/5a800174-7ced-486e-9880-c5feac4d44cb)


## 2. Subnetze erstellen

Im nächsten Schritt habe ich zwei Subnetze angelegt: ein öffentliches Subnetz und ein privates Subnetz. Das öffentliche Subnetz dient dazu, den Webserver mit dem Internet zu verbinden, während das private Subnetz isoliert bleibt, um interne Dienste zu schützen.

### Screenshot: Erstellen der Subnetze

![image](https://github.com/user-attachments/assets/2b203cf4-7ecb-49d5-8ce2-dd79bcfc366b)


## 3. Routing-Tabellen konfigurieren

Um sicherzustellen, dass das öffentliche Subnetz Internetzugang hat, habe ich eine Routing-Tabelle erstellt, die das Internet-Gateway mit dem Subnetz verbindet. Gleichzeitig habe ich die Routing-Tabelle für das private Subnetz so konfiguriert, dass es über einen NAT-Gateway ins Internet zugreifen kann.

### Screenshot: Routing-Tabelle

![image](https://github.com/user-attachments/assets/91dd48d1-828b-4253-b8d2-1d65faa6add6)


## 4. Security Group erstellen

Als nächstes habe ich eine Security Group erstellt, um den Zugriff auf die EC2-Instanz zu regeln. In dieser Security Group habe ich HTTP-Zugriff aus dem Internet erlaubt, um den Webserver erreichbar zu machen. Ich habe auch nachträglich SSH-Zugriff hinzugefügt, um bei Bedarf über die Konsole auf den Server zugreifen zu können.

### Screenshot: Security Group erstellen

![image](https://github.com/user-attachments/assets/717e332d-b959-427f-b095-a0d579e48cd0)


## 5. EC2-Instanz erstellen

Nun habe ich eine EC2-Instanz in der VPC gestartet. Dabei habe ich sichergestellt, dass die Instanz im öffentlichen Subnetz liegt und die Security Group mit HTTP- und SSH-Zugriff zugewiesen wurde. Die Instanz dient als Webserver und wird später für den Zugriff auf die Webseite genutzt.

### Screenshot: EC2-Instanz erstellen

![image](https://github.com/user-attachments/assets/8a7fd129-6f00-4a95-b263-603e63a66e01)


## 6. Test des Webservers

Nach dem erfolgreichen Start der EC2-Instanz konnte ich über die zugewiesene öffentliche IP-Adresse auf den Webserver zugreifen. Ich habe sowohl die Startseite als auch eine zusätzliche PHP-Seite (`load.php`) getestet.

### Screenshot: Webseite (IP-Adresse und load.php)

![image](https://github.com/user-attachments/assets/15258f42-f3f1-4fe9-95ca-1a9f5f1b6422)


![image](https://github.com/user-attachments/assets/de8d9f76-ba43-4382-897d-316f43071042)


## Fazit

Es hat ein paar Versuche gebraucht, um die VPC und Subnetze korrekt zu erstellen, aber am Ende konnte ich erfolgreich einen Webserver bereitstellen. Die Public- und Private-Subnetze dienen dazu, Dienste voneinander zu trennen: Öffentlich zugängliche Dienste im öffentlichen Subnetz und interne Dienste im privaten Subnetz. Der Webserver konnte erfolgreich über das Internet erreicht werden, während der Datenverkehr aus dem privaten Subnetz über das NAT-Gateway geroutet wurde.


