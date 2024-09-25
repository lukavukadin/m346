# Modul 4: Virtuelle Server

## Modulzweck
In diesem Modul lernst du, wie du eine Amazon Elastic Compute Cloud (Amazon EC2) Instanz erstellst und diese zum Hosten einer Website verwendest. Du wirst auch den Zweck von Zugriffsschlüsseln, dem Domain Name System (DNS), Amazon Route 53 und Virtual Private Clouds kennenlernen.

## Fragen

1. **Denken Sie an eine Website oder App, die Sie regelmäßig nutzen. Was ist der Zweck dieser Website oder App für den Nutzer und für den Entwickler? Sind diese Zwecke ähnlich oder unterschiedlich?**
   - **App:** Handy-Spiel  
   - **Zweck für den Nutzer:** Als Nutzer spiele ich das Spiel, um mich zu unterhalten und Spaß zu haben.  
   - **Zweck für den Entwickler:** Der Entwickler integriert Werbung in das Spiel, um Einnahmen zu generieren.  
   - **Zusammenfassung:** Während ich als Nutzer Unterhaltung suche, nutzt der Entwickler die Plattform, um durch Werbung Geld zu verdienen. Die Zwecke sind zwar miteinander verbunden, aber letztlich unterschiedlich.

2. **Welche Faktoren sind wichtig bei der Namensgebung einer Website und warum? Wie beeinflusst der Name das Nutzererlebnis und die Eindrücke der Website? Welche zwei Faktoren sind dir am wichtigsten bei der Namenswahl?**
   - **Wichtige Faktoren bei der Namensgebung:** Ein Name sollte eindeutig und nicht verwechselbar mit anderen sein. Er sollte kurz, einprägsam und leicht merkbar sein.  
   - **Beispiel:** Der neue Name von Twitter, "X", ist ein interessantes Beispiel. Designtechnisch ist der Name minimalistisch, aber viele Nutzer identifizieren die Plattform weiterhin als "Twitter". Der Name "X" ist so kurz, dass er für eine App nicht aussagekräftig genug erscheint.  
   - **Zwei wichtige Faktoren:** Eindeutigkeit und Wiedererkennungswert sind für mich am wichtigsten. Ein klarer, prägnanter Name bleibt im Gedächtnis und sorgt dafür, dass die Website leicht gefunden und wiedererkannt wird.

3. **Viele Websites speichern Daten über Ihre Nutzung, entweder als Cookies auf Ihrem Computer oder auf der Website selbst. Ist der Austausch von Daten gegen einen kostenlosen Dienst gerechtfertigt? Sollte mehr Transparenz darüber herrschen, welche Daten gesammelt werden, und sollten Sie die Möglichkeit haben, dies zu verhindern?**
   - **Meine Meinung:** Es ist schwierig, eine klare Alternative zum aktuellen Modell zu finden, in dem Websites durch Datensammlung finanziert werden. Eine Verbesserung wäre, wenn Websites sich nur durch Werbung finanzieren würden und nicht durch den Verkauf von Nutzerdaten.  
   - **Transparenz:** Websites sollten transparenter darüber informieren, welche Daten gesammelt werden, und es sollte stets die Möglichkeit geben, sich von der Datensammlung abzumelden. Dies würde das Vertrauen der Nutzer stärken und die Privatsphäre besser schützen.

## Aktivität 1: Erstellen einer EC2-Instanz

### Übersicht
In dieser Aktivität wirst du eine Amazon EC2-Instanz erstellen und eine Website darauf hosten.

### Ziele
- Eine EC2-Instanz erstellen und verwalten.
- Eine einfache Website auf der Instanz hosten.

### Wichtige Technologien
- **Amazon EC2:** Bietet skalierbare Rechenleistung in der Cloud. Ermöglicht die Ausführung von Anwendungen auf virtuellen Maschinen.  
- **Amazon S3:** Ein Cloud-basierter Speicher für Daten, nützlich für Backups oder zum Hosten von statischen Websites.  
- **Domain Name System (DNS):** Ein System zur Verwaltung von Namen und IP-Adressen im Internet.  
- **Amazon Route 53:** Der DNS-Dienst von AWS, der Domainnamen verwaltet und Traffic auf Webanwendungen leitet.  
- **Virtual Private Cloud (VPC):** Eine isolierte Netzwerkumgebung in AWS, die zur sicheren Verwaltung von Ressourcen dient.
