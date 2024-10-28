## Zwei Webserver erstellen und Last mittles Load Balancer gleichmässig verteilen


### 1. Zuerst habe ich die erste EC2 Webserver 1 Instance erstellt

![image](https://github.com/user-attachments/assets/46b27692-0dab-4bd2-9053-550cd50648cf)


---

### 2. Dann habe ich den Webserver geöffnet mit der IPv4

![image](https://github.com/user-attachments/assets/9e41671c-1cc7-46cf-80a9-de31cadf7743)


---

### 3. Nun habe ich die EC2-Instanz *Webserver 2* erstellt. Dies habe ich über Aktionen -> Image und Vorlagen --> weitere ähnliche Elemente auswählen. Dort muss man dann nur noch den Namne ändern der Instance und einen andere Sicherheitsgruppe auswäheln, bei uns jetzt us-east.1b

![image](https://github.com/user-attachments/assets/8137c7c4-ce20-4427-a55d-e6b5df7621eb)


![image](https://github.com/user-attachments/assets/26000bfb-3b59-4155-bdd2-e88f8024a0cd)

---

### 4. Hier sieht man das ich den Webserver 2 öffnen konnte


![image](https://github.com/user-attachments/assets/3511d529-4f1d-45b6-bedb-b57161f6bb4f)



---
### 5. Jetzt habe ich den Load Balancer erstellt. Hier habe ich Application Load Balancer ausgewählt, weil es verfügbar für viele Funktionen und kann verwendet werden für HTTP und HTTPS-Verkehr.


![image](https://github.com/user-attachments/assets/12ccf0d1-160b-44a2-b93f-2e8bc3fb7dc0)



---
### 6. Hier sieht man den erstellten Load Balancer er ist Aktiv und unten rechts sieht man den DNS-Namen


![image](https://github.com/user-attachments/assets/d2597a30-67b6-44bb-aaee-1aef64dec96b)


---

### 7. In diesem Bild sieht man das anzeigen von Webserver 1


![image](https://github.com/user-attachments/assets/f425ab0b-cad0-42b1-a53c-763497858f88)

---

### 8. Nach mehrmals laden der Seite sieht man jetzt das Anzeigen von Webserver 2. Es hat funktioniert ich bin sehr froh


![image](https://github.com/user-attachments/assets/c341e9cf-999d-4766-a7cf-2e57ff06153c)


----
## Fazit

Durch die Erstellung und Konfiguration von zwei EC2-Webservern sowie die Implementierung eines Load Balancers habe ich praktische Erfahrungen im Bereich Cloud-Computing gesammelt. Der Load Balancer ermöglicht eine gleichmäßige Verteilung des Datenverkehrs auf beide Webserver, was die Verfügbarkeit und Skalierbarkeit meiner Anwendung verbessert. Insgesamt hat mir dieser Prozess ein besseres Verständnis für die Funktionsweise von Load Balancing in der Cloud vermittelt.
