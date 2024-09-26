## Cloud init

**Sie kennen die Grundelemente von YAML und erkennen diese in Cloud-init Dateien?**

Dateiformat und Header: Cloud-init Datein beginnen oft mit dem Header #cloud-config. Dies zeigt an das es sich um eine YAML-Datei handelt.

Es gibt noch weitere Merkmale, aber diese ist am einfachsten zu sehen.

**Sie können die Vorteile von Cloud-init erläutern.**

1. Die Instanzen werden beim Start automatisch konfiguriert.
2. Unterstützt viele Cloud-Anbieter
3. leicht verständliche Konfigurationsdatei

**Sie kennen die wichtigsten Elemente von Cloud-init und können diese auch anwenden.**

Die wichtigsten Elemente sind: 

Header: #cloud-config
users: ....mit dem kann man den Benutzer erstellen
packages installieren: automatisches installieren von Softwarepaketen 
runcmd: Befehle ausführen

**Sie können eine virtuelle Instanz mit Cloud-init installieren.**

Man erstellst ein Cloud-init Skript, fügt es beim Erstellen der Instanz als "User Data" hinzu und startet die Instanz. Cloud-init übernimmt dann die Konfiguration beim ersten Boot.



**Sie kennen den Begriff "Infrastructure As Code" und können ihn erklären.**

**Infrastructure as Code** (IaC) ist ein Ansatz zur automatisierten Verwaltung von Infrastruktur. Mit IaC können Instanzen in der Cloud schnell und konsistent bereitgestellt werden, indem die Konfiguration als Code definiert wird. Dies erhöht die Effizienz und verringert menschliche Fehler.

**Vorteile von IaC**

- **Schnelle Bereitstellung**: Ressourcen können in Minuten erstellt werden.
- **Konsistenz**: Gleiche Konfigurationen werden jedes Mal gleich umgesetzt.
- **Versionierung**: Änderungen sind nachvollziehbar und können zurückgesetzt werden.
- **Automatisierung**: Minimiert manuelle Eingriffe und Fehler.

## Beispiel für IaC

Hier ist ein einfaches Beispiel für IaC mit einem AWS-Instanz zu erstellen:

```hcl
resource "aws_instance" "mein-server" {
  ami           = "ami-12345678"
  instance_type = "t2.micro"
}










