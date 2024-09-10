# AWS On-Demand Pricing und Instanzvergleich

## Ausgangslage
In dieser Übung haben wir die AWS Management Console verwendet, um das On-Demand Pricing-Modell von Amazon EC2 kennenzulernen. Der Fokus lag auf einem Vergleich zwischen den Instanztypen **t2.micro** und **m4.xlarge** für eine Laufzeit von einem Monat. Zudem wurden mögliche Use-Cases für beide Instanztypen untersucht.

---

## Kostenkalkulation

Für die Region **North Virginia (us-east-1)** gelten folgende On-Demand Preise:

| Instanztyp  | Stündlicher Preis (USD) | Monatlicher Preis (USD) |
|-------------|-------------------------|-------------------------|
| **t2.micro** | $0.0116                 | 8.35                    |
| **m4.xlarge** | $0.2                    | 144                     |

**Berechnung der monatlichen Kosten:**

- **t2.micro**:
  \[
  0.0116 \, \text{USD} \times 24 \, \text{Stunden} \times 30 \, \text{Tage} = 8.35 \, \text{USD}
  \]

- **m4.xlarge**:
  \[
  0.2 \, \text{USD} \times 24 \, \text{Stunden} \times 30 \, \text{Tage} = 144 \, \text{USD}
  \]

**Monatliche Kostenübersicht:**
- **t2.micro**: 8.35 USD
- **m4.xlarge**: 144 USD

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
Der Vergleich zeigt, dass **t2.micro** für kostengünstigere und weniger leistungsintensive Anwendungen geeignet ist, während **m4.xlarge** für leistungsintensive Aufgaben und größere Workloads besser geeignet ist. Die Wahl des Instanztyps sollte basierend auf den spezifischen Anforderungen und dem Budget der jeweiligen Anwendung getroffen werden.
