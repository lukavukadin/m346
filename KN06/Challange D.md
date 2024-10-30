# Load Balancer / High Availability

### 1. Zuerst habe ich die Zielgruppe erstellt mit den zwei Instanzen. Es ist noch kein Load Balancer zugewiesen, dies müssen wir noch machen.

![image](https://github.com/user-attachments/assets/c6839a92-e136-4fe8-884c-d3043333292e)

---

### 2. Jetzt habe ich den Load Balancer erstellt.

![image](https://github.com/user-attachments/assets/6e73a5f3-2569-498d-9ea0-2be069a43a31)

---

### 3. Dann musste ich die Auto Scaling Group der Target Group des Load Balancers zuweisen.

![image](https://github.com/user-attachments/assets/e1414100-00db-4857-84e3-afa65c372fcd)

---

### 4. Nun musste ich unter Load Balancer den DNS-Namen kopieren und ihn im Browser öffnen:  
**"KN06-VUK-ALB1-1958285208.us-east-1.elb.amazonaws.com"**

![image](https://github.com/user-attachments/assets/88a91bab-b7f0-444f-95e4-171ea4d4ebf8)

---

### 5. Hier sieht man die erfolgreiche Verbindung. Wenn man die Seite neu lädt, wechselt es zwischen den beiden Instanzen.

![image](https://github.com/user-attachments/assets/2b9f02c6-f0bf-4ed3-85a0-787da45b9a11)

![image](https://github.com/user-attachments/assets/a37f61d6-71c0-4835-b992-26d0bfe74714)

---

### Fazit
Die Implementierung des Load Balancers in Verbindung mit der Auto Scaling Group verlief reibungslos. Durch die korrekte Konfiguration wurde sichergestellt, dass die Anfragen gleichmäßig auf die beiden Instanzen verteilt werden. Die erfolgreiche Verbindung wurde durch die Funktionsprüfung über den DNS-Namen des Load Balancers bestätigt. Die Automatisierung und Fehlertoleranz der Architektur sorgen dafür, dass die Plattform hochverfügbar ist. Dies ermöglicht eine robuste Nutzung, selbst wenn eine Instanz ausfällt. Insgesamt bin ich mit dem Ergebnis sehr zufrieden.



