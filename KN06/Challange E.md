# High Availability Setup mit elastischer Anpassung der Ressourcen (HA Ninja)



### 1. Zuerst habe ich mit den Angaben von der Anleitung eine neue Launch Templates mit dem Namen KN06_VUK_LaunchTemplate_2 erstellt.


![image](https://github.com/user-attachments/assets/d9f3f693-e136-4ff1-aa5f-2d8b6ffeede4)



---

### 2. Jetzt habe ich eine neue Auto Scaling Group erstellt mit dem Namen KN06_VUK_AutoScalingGroup_2


![image](https://github.com/user-attachments/assets/d4809fc2-d055-4e17-a351-e4624cfda153)


---

### 3. Hier sieht man das die beiden Instancen in einer unterschiedlichen Availability Zones liegen und der Status active ist.




---

### 4. Nun musste ich die Target Group erstellen.



---

### 5. In diesem Schritt musste ich einen neuen Lad Balancer erstellen mit dem namen KN06-VUK-ALB2.



---

### 6. Jetzt musste ich den Auto Scaling Group der Target Group des Load Balancer zuweisen




---

### 7. Nun einen Dynamic Scaling policy erzeugen und einbinden





---

### 8. Beweis

---

### Fazit


