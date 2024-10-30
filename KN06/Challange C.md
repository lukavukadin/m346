# Auto Scaling Group erstellen und anwenden

### 1. Zuerst habe ich einen Launch Templates mit hilfe der Anleitung erstellt.

![image](https://github.com/user-attachments/assets/47e83b35-b90c-4427-8aaa-9ffd12383747)




---

### 2. In disesem Schritt habe ich die Auto-Scaling-Gruppe erstellt, mit us-east-1a und -1b.

![image](https://github.com/user-attachments/assets/1954d5a8-ad76-4b88-8f75-59baf4a2ee34)




### 3. Hier sieht man das di ebeiden Instancen in einer unterschiedlichen Availability Zones liegen


![image](https://github.com/user-attachments/assets/035d0033-85cd-4c2f-8d73-bba84e84a55f)


---

### 3. Hier sieht man den erfolgreichen Zugriff auf die Instance us-east-1a


![image](https://github.com/user-attachments/assets/ed69135b-be21-4175-b5f4-b54896900498)




---

### 4. Hier sieht man den erfolgreichen Zugriff auf die Instance us-east-1b

![image](https://github.com/user-attachments/assets/ecae21c3-b379-4306-89d9-462e2fa19728)



---

### Fazit


In diesem Projekt habe ich erfolgreich eine **Auto Scaling Group** erstellt und angewendet, die zuverlässig zwei EC2-Instanzen in den Availability Zones **us-east-1a** und **us-east-1b** betreibt.

Das Erstellen der **Auto Scaling Group** verlief größtenteils reibungslos, aber es gab ein paar Stolpersteine. Insbesondere musste ich in den **Subnetzeinstellungen von us-east-1a** die automatische IP-Zuweisung aktivieren, da die Instanz sonst nicht erreichbar war. 

Mit dieser Anpassung konnte ich die Verfügbarkeit und Stabilität der Instanzen sicherstellen und die Auto Scaling Group erfolgreich konfigurieren.


