# Vergleich von Cloud-Providern: AWS vs. Microsoft Azure

## Ausgangslage
In dieser Übung vergleichen wir AWS mit Microsoft Azure, einem weiteren großen Cloud-Provider. Ziel ist es, die Kosten und Funktionen der beiden Cloud-Plattformen zu vergleichen und die beste Lösung für die Anforderungen eines Unternehmens mit 50 Mitarbeitern zu empfehlen.

## Schritt 1: Provider-Auswahl
Für den Vergleich haben wir **Microsoft Azure** ausgewählt.

## Schritt 2: Funktionen und Services

### AWS (Referenz)
- **EC2 t2.micro**: Kleine, kostengünstige Instanz für grundlegende Anwendungen.
- **S3**: Speicherdienst für Datenhaltung.

### Microsoft Azure
- **Azure Virtual Machines B1s**: Entspricht der t2.micro-Instanz von AWS.
- **Azure Blob Storage**: Entspricht dem S3-Speicher von AWS.

## Schritt 3: Kostenvergleich

### AWS Kosten (aus der vorherigen Übung)
- **EC2 t2.micro**: 8.60 USD/Monat
- **S3-Speicher 20TB**: 4.00 USD/Monat
- **Gesamtkosten AWS Low**: 1'012.60 USD/Monat

### Microsoft Azure Kosten

#### Azure Virtual Machines B1s
- **Kosten pro Monat:** 8.50 USD (geschätzt)

#### Azure Blob Storage 20TB
- **Kosten pro Monat:** 4.20 USD (geschätzt)

#### Gesamtkosten Azure
- **Monatliche Gesamtkosten Azure**: 8.50 USD + 4.20 USD = 12.70 USD
- **Jährliche Gesamtkosten Azure:** 12.70 USD * 12 = 152.40 USD
- **Kosten auf 3 Jahre:** 152.40 USD * 3 = 457.20 USD

## Schritt 4: Performance und Verfügbarkeit

### AWS
- **EC2 t2.micro:** Gute Leistung für grundlegende Anwendungen; geeignet für Web-Server und kleine Datenbanken.
- **S3:** Hohe Verfügbarkeit und Durabilität; zuverlässiger Speicherdienst.

### Microsoft Azure
- **Azure Virtual Machines B1s:** Vergleichbare Leistung mit t2.micro; ebenfalls gut für einfache Web-Server und Entwicklungsumgebungen.
- **Azure Blob Storage:** Hohe Verfügbarkeit und Performance; vergleichbar mit AWS S3.

### Unterschiede in der Leistung
Beide Anbieter bieten vergleichbare Leistungen und Verfügbarkeiten. Die Unterschiede können sich jedoch je nach spezifischen Anforderungen und geographischer Lage unterscheiden. Azure und AWS bieten beide SLAs (Service Level Agreements) für Verfügbarkeit und Performance.

## Schritt 5: Vor- und Nachteile

### AWS
**Vorteile:**
- **Etablierter Marktführer:** Große Verbreitung und bewährte Dienste.
- **Vielseitigkeit:** Umfangreiche Auswahl an zusätzlichen Services.
- **Globale Reichweite:** Zahlreiche Rechenzentren weltweit.

**Nachteile:**
- **Kostenstruktur:** Kann komplex sein, insbesondere bei zusätzlichem Traffic und Datenübertragung.
- **Kundensupport:** Unterschiedliche Erfahrungsberichte.

### Microsoft Azure
**Vorteile:**
- **Integration:** Gute Integration mit Microsoft-Produkten und -Diensten.
- **Preisgestaltung:** Leicht günstigere Einstiegspreise im Vergleich zu AWS für vergleichbare Dienste.
- **Hybrid-Cloud-Optionen:** Starke Unterstützung für hybride Cloud-Szenarien.

**Nachteile:**
- **Marktanteil:** Weniger verbreitet als AWS in einigen Regionen.
- **Dokumentation:** Weniger umfassende Dokumentation und Community-Ressourcen als AWS.

## Empfehlung

Basierend auf der Kostenanalyse und den verfügbaren Funktionen bietet **Microsoft Azure** eine kostengünstigere Lösung als AWS. Die Preise für Azure Virtual Machines und Blob Storage sind günstiger als die vergleichbaren AWS-Dienste. 

**Empfohlene Lösung:**

1. **Migration zu Microsoft Azure:** Die Kostenvorteile und die enge Integration mit Microsoft-Produkten können für viele Unternehmen vorteilhaft sein.
2. **Weitere Evaluierung:** Es ist ratsam, spezifische Anforderungen des Unternehmens zu berücksichtigen und möglicherweise eine Testmigration durchzuführen, um die Eignung der Plattform zu überprüfen.

---

**Leistungsnachweis:**

- Vergleich der Kosten und Funktionen von AWS und Microsoft Azure.
- Analyse der Performance und Verfügbarkeit der beiden Cloud-Provider.
- Differenzierte und nachvollziehbare Dokumentation der Ergebnisse.
- Präsentation der Ergebnisse und Fachgespräch mit Coach.

