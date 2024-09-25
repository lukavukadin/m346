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

Im Folgenden sind die drei wichtigen Schritte zur Erstellung einer EC2-Instanz zusammengefasst:

## Aktivität 1: Erstellen einer EC2-Instanz

Im Folgenden sind die drei wichtigen Schritte zur Erstellung einer EC2-Instanz zusammengefasst:

### 1. Erstellen der EC2-Instanz

Im ersten Schritt habe ich eine EC2-Instanz mit dem Namen **Web Server 1** erstellt. Auf dem Screenshot sieht man die **öffentliche IPv4-Adresse**, mit der die Website abgerufen werden kann. Damit dies jedoch funktioniert, musste eine Sicherheitsregel erstellt werden, um den Zugriff zu erlauben.

<img src="https://github.com/user-attachments/assets/c54b63f8-b3aa-4f66-ba70-48ed1f730ee1" alt="EC2 Instanz erstellt" width="30%"/>

### 2. Erstellen der Sicherheitsregel

Um den Zugriff auf den Webserver zu ermöglichen, musste eine **Sicherheitsregel** hinzugefügt werden, die den HTTP-Verkehr zulässt. Dies erlaubt es, über den Browser auf die Website zuzugreifen. Auf dem Bild ist die erstellte Regel zu sehen, die sicherstellt, dass die Website nun erreichbar ist.

<img src="https://github.com/user-attachments/assets/c4ba4ed0-0f17-47f1-865e-14998e428656" alt="Sicherheitsregel erstellt" width="30%"/>

### 3. Website-Abruf

Nachdem die Sicherheitsregel erfolgreich hinzugefügt wurde, konnte ich die Website aufrufen. Die Website hat den Text **"Hello World"** korrekt ausgegeben, was zeigt, dass der Webserver erfolgreich läuft.

<img src="https://github.com/user-attachments/assets/c94aa32b-ea90-49e0-a533-e5444c44d261" alt="Website mit Hello World" width="30%"/>


