# Cloud-init und Infrastructure as Code (IaC)

## Einführung in Cloud-init

Cloud-init ist ein Tool, das die automatische Konfiguration von Cloud-Instanzen beim Start ermöglicht. Hier sind die Grundelemente und Vorteile von Cloud-init:

### Grundelemente von YAML in Cloud-init

Cloud-init-Dateien beginnen oft mit dem Header `#cloud-config`, der signalisiert, dass es sich um eine YAML-Datei handelt. YAML (YAML Ain't Markup Language) ist ein menschenlesbares Datenformat, das für Konfigurationsdateien verwendet wird. Hier sind einige weitere Merkmale:

- **Einfache Syntax**: Klar strukturierte Daten mit Einrückungen.
- **Schlüssel-Wert-Paare**: Daten werden in einem leicht verständlichen Format dargestellt.

### Vorteile von Cloud-init

1. **Automatische Konfiguration**: Instanzen werden beim Start automatisch konfiguriert, was den Einrichtungsaufwand reduziert.
2. **Unterstützung für viele Cloud-Anbieter**: Cloud-init funktioniert auf einer Vielzahl von Plattformen, darunter AWS, Azure und Google Cloud.
3. **Einfache Konfiguration**: Die Verwendung von YAML macht die Konfiguration leicht verständlich und wartbar.

### Wichtige Elemente von Cloud-init

Die wichtigsten Elemente, die Sie in Cloud-init verwenden können, sind:

- **Header**: `#cloud-config`
- **users**: Erstellen und Konfigurieren von Benutzern.
- **packages**: Automatische Installation von Softwarepaketen.
- **runcmd**: Ausführen von Shell-Befehlen während des Bootvorgangs.

### Installation einer virtuellen Instanz mit Cloud-init

Um eine virtuelle Instanz mit Cloud-init zu installieren, folgen Sie diesen Schritten:

1. Erstellen Sie ein Cloud-init-Skript.
2. Fügen Sie das Skript beim Erstellen der Instanz als "User Data" hinzu.
3. Starten Sie die Instanz.

Cloud-init übernimmt die Konfiguration während des ersten Bootvorgangs.

## Infrastructure as Code (IaC)

### Definition

**Infrastructure as Code** (IaC) ist ein Ansatz zur automatisierten Verwaltung von Infrastruktur. Mit IaC können Cloud-Ressourcen schnell und konsistent bereitgestellt werden, indem die Konfiguration als Code definiert wird. Dies erhöht die Effizienz und verringert menschliche Fehler.

### Vorteile von IaC

- **Schnelle Bereitstellung**: Ressourcen können in Minuten erstellt werden.
- **Konsistenz**: Gleiche Konfigurationen werden jedes Mal gleich umgesetzt.
- **Versionierung**: Änderungen sind nachvollziehbar und können zurückgesetzt werden.
- **Automatisierung**: Minimiert manuelle Eingriffe und Fehler.

### Beispiel für IaC

Hier ist ein einfaches Beispiel für IaC zur Erstellung einer AWS-Instanz:

```hcl
resource "aws_instance" "mein-server" {
  ami           = "ami-12345678"
  instance_type = "t2.micro"
}
