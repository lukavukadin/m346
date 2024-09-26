# Evaluation Cloud-Migration für ein Unternehmen mit 50 Mitarbeitern

## Ausgangslage

Das Unternehmen mit 50 Mitarbeitern betreibt derzeit die IT On-Premises. Die monatlichen IT-Kosten setzen sich aus verschiedenen Faktoren zusammen, darunter ein NAS-Speicher von 20 TB. Die Hardware wird über 3 Jahre abgeschrieben. Ziel ist es, herauszufinden, ob eine Migration zur AWS-Cloud wirtschaftlich sinnvoll wäre und wie viel Geld gespart werden kann, wenn man alle drei Varianten auf 3 Jahre hochrechnet. Diese Übung umfasst nur EC2-Instanzen und S3-Speicher.

---

## Schritt 1: Kostenanalyse On-Premises

### Fixkosten pro Monat

| Kostenart                         | Betrag    |
|-----------------------------------|-----------|
| Raummiete                         | 1'000.-   |
| Administration (20% Stelle)        | 1'000.-   |
| Server (HPE Proliant)              | 2'500.-   |
| Netzwerk und weitere Geräte        | 2'500.-   |
| Diverses (Lizenzen etc.)           | 2'500.-   |
| **Gesamtkosten On-Premises**       | **9'500.-** |

---

## Schritt 2a: Kostenanalyse Variante Low - AWS Instance-Type t2.micro

### Kosten pro Monat

| Kostenart                          | Betrag   |
|------------------------------------|----------|
| AWS EC2 t2.micro (Var. A)           | 11.66 USD |
| AWS S3-Speicher 20TB                | 471.04 USD|
| Weitere Kosten (Administration etc.)| 2'000.-   |
| **Gesamtkosten AWS Low**            | **2'482.70 USD** |

**Jährliche Gesamtkosten AWS Low:** 2'482.70 USD * 12 = 29'792.40 USD  
**Kosten auf 3 Jahre:** 29'792.40 USD * 3 = 89'377.20 USD

---

## Schritt 2b: Kostenanalyse Variante X-Large - AWS Instance-Type m4.xlarge

### Kosten pro Monat

| Kostenart                          | Betrag   |
|------------------------------------|----------|
| AWS EC2 m4.xlarge (Var. B)          | 143.28 USD|
| AWS S3-Speicher 20TB                | 471.04 USD|
| Weitere Kosten (Administration etc.)| 2'000.-   |
| **Gesamtkosten AWS X-Large**        | **2'614.32 USD** |

**Jährliche Gesamtkosten AWS X-Large:** 2'614.32 USD * 12 = 31'371.84 USD  
**Kosten auf 3 Jahre:** 31'371.84 USD * 3 = 94'115.52 USD

---

## Schritt 3: Vergleich der drei Varianten

| Variante         | Pro Monat | Pro Jahr   | 3 Jahre    |
|------------------|-----------|------------|------------|
| On-Premises       | 9'500.-   | 114'000.-   | 342'000.-  |
| t2.micro          | 2'482.70.- | 29'792.40.- | 89'377.20.-|
| m4.xlarge         | 2'614.32.-| 31'371.84-   | 94'115.52.-  |

---

## Schritt 4: Vorteile und Nachteile der Cloud


### Vorteile
- **Flexibilität:** Hohe Skalierbarkeit nach Bedarf, keine Überprovisionierung nötig.
- **Wartung:** Keine Hardware-Wartung oder Erneuerung erforderlich.
- **Kostenkontrolle:** Anpassung der Ressourcen basierend auf der tatsächlichen Nutzung.
- **Zugänglichkeit:** Zugriff auf die neuesten Technologien und globale Verfügbarkeit.

### Nachteile
- **Langfristige Kosten:** Höhere monatliche Ausgaben im Vergleich zu On-Premises-Lösungen, vor allem bei leistungsstarken Instanzen.
- **Abhängigkeit von Internet:** Ständige Internetverbindung erforderlich.
- **Sicherheitsbedenken:** Daten müssen auf Drittanbieter-Servern gespeichert werden.

---

## Schritt 5: Empfehlung Lösungsvorschlag

Auf Basis der Kostenanalyse empfehle ich die **AWS EC2 t2.micro**-Instanz. Diese Option ist viel günstiger als die On-Premises-Lösung und die größere m4.xlarge-Instanz. Für ein kleines Unternehmen mit 50 Mitarbeitern ist sie gut geeignet und spart Geld.

**Vorschlag:**

1. **Wechsel zu AWS EC2 t2.micro und S3:** Günstig und erfüllt die grundlegenden Anforderungen.
2. **Weitere Prüfung:** Es ist sinnvoll, genau zu prüfen, welche weiteren AWS-Dienste benötigt werden.

Insgesamt spart die Cloud-Migration zu EC2 t2.micro und S3 Geld. Eine genauere Analyse sollte jedoch erfolgen, um alle Bedürfnisse zu berücksichtigen.

## Quellen

- Ich habe das GitLab-Dokument von Callisto Migartion_Cloud  durchgelesen. Dann habe ich bei der AWS console die Instancen verglichen und die Preise an ChatGPT geben, damit er mir die Tabelle erstellt.

---

## Credits
- Martin hat mir geholfen zu erklären was der unterschied zwischen den zwei Varianten ist
