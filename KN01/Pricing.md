# AWS On-Demand Pricing und Instanzvergleich

## Ausgangslage
In dieser Übung habe ich die AWS Management Console verwendet, um das On-Demand Pricing-Modell von Amazon EC2 kennenzulernen. Der Fokus lag auf einem Vergleich zwischen den Instanztypen **t2.micro** und **m4.xlarge** für eine Laufzeit von einem Monat. Zudem wurden mögliche Use-Cases für beide Instanztypen gesucht.

---

## Kostenkalkulation

Für die Region **North Virginia (us-east-1)** gelten folgende On-Demand Preise:

| Instanztyp   | Stündlicher Preis (USD) | Monatlicher Preis (USD)       |
|--------------|--------------------------|-------------------------------|
| **t2.micro** | $0.0162                  | $0.0162 × 24 × 30 = $11.66    |
| **m4.xlarge**| $0.384                     | $0.384 × 24 × 30 = $276.48    |

---

## Use-Cases

### t2.micro
- **Geeignet für**:
  - Kleine Webserver
  - Entwicklungs- und Testumgebungen
  - Microservices
  - Anwendungen mit geringem Traffic und Ressourcenbedarf

### m4.xlarge
- **Geeignet für**:
  - Datenbankserver
  - Datenintensive Anwendungen
  - Verteilte Systeme
  - Machine Learning-Workloads

---

## Fazit
**t2.micro** ist gut für einfache und günstige Anwendungen. **m4.xlarge** ist besser für anspruchsvollere Aufgaben und grössere Datenmengen. Die Wahl hängt davon ab, was die Anwendung braucht und wie viel Budget zur Verfügung steht.
