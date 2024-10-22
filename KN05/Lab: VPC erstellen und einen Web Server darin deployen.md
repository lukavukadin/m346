# VPC erstellen und Webserver darin deployen

## Was ist eine VPC?

Eine Virtual Private Cloud (VPC) ist ein privates Netzwerk in der Cloud, das man vollständig kontrollieren kann. Es ermöglicht die Bereitstellung und Verwaltung von Servern oder anderen Ressourcen innerhalb eines isolierten Netzwerks.

## VPC erstellen

Zuerst habe ich eine neue VPC erstellt, in der ich später den Webserver betreiben werde. Dies geschieht über die AWS Management Console, wo man die grundlegenden Netzwerkeinstellungen wie CIDR-Blöcke und Subnetze festlegt.

### Screenshot: VPC Workflow erstellen

![VPC Workflow erstellen](path/to/screenshot_vpc.png)

## Subnetze erstellen

Im nächsten Schritt habe ich zwei Subnetze angelegt: ein öffentliches Subnetz und ein privates Subnetz. Das öffentliche Subnetz dient dazu, den Webserver mit dem Internet zu verbinden, während das private Subnetz isoliert bleibt, um interne Dienste zu schützen.

### Screenshot: Erstellen der Subnetze

![Subnetze erstellen](path/to/screenshot_subnets.png)

## Routing-Tabellen konfigurieren

Um sicherzustellen, dass das öffentliche Subnetz Internetzugang hat, habe ich eine Routing-Tabelle erstellt, die das Internet-Gateway mit dem Subnetz verbindet. Gleichzeitig habe ich die Routing-Tabelle für das private Subnetz so konfiguriert, dass es über einen NAT-Gateway ins Internet zugreifen kann.

### Screenshot: Routing-Tabelle

![Routing-Tabelle](path/to/screenshot_routing_table.png)

## Security Group erstellen

Als nächstes habe ich eine Security Group erstellt, um den Zugriff auf die EC2-Instanz zu regeln. In dieser Security Group habe ich HTTP-Zugriff aus dem Internet erlaubt, um den Webserver erreichbar zu machen. Ich habe auch nachträglich SSH-Zugriff hinzugefügt, um bei Bedarf über die Konsole auf den Server zugreifen zu können.

### Screenshot: Security Group erstellen

![Security Group erstellen](path/to/screenshot_security_group.png)

## EC2-Instanz erstellen

Nun habe ich eine EC2-Instanz in der VPC gestartet. Dabei habe ich sichergestellt, dass die Instanz im öffentlichen Subnetz liegt und die Security Group mit HTTP- und SSH-Zugriff zugewiesen wurde. Die Instanz dient als Webserver und wird später für den Zugriff auf die Webseite genutzt.

### Screenshot: EC2-Instanz erstellen

![EC2-Instanz erstellen](path/to/screenshot_instance.png)

## Test des Webservers

Nach dem erfolgreichen Start der EC2-Instanz konnte ich über die zugewiesene öffentliche IP-Adresse auf den Webserver zugreifen. Ich habe sowohl die Startseite als auch eine zusätzliche PHP-Seite (`load.php`) getestet.

### Screenshot: Webseite (IP-Adresse und load.php)

![Webseite mit IP-Adresse](path/to/screenshot_website_ip.png)

![Webseite mit load.php](path/to/screenshot_website_load_php.png)

## Fazit

Es hat ein paar Versuche gebraucht, um die VPC und Subnetze korrekt zu erstellen, aber am Ende konnte ich erfolgreich einen Webserver bereitstellen. Die Public- und Private-Subnetze dienen dazu, Dienste voneinander zu trennen: Öffentlich zugängliche Dienste im öffentlichen Subnetz und interne Dienste im privaten Subnetz. Der Webserver konnte erfolgreich über das Internet erreicht werden, während der Datenverkehr aus dem privaten Subnetz über das NAT-Gateway geroutet wurde.


