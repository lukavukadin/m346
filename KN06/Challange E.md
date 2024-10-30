# High Availability Setup mit elastischer Anpassung der Ressourcen (HA Ninja)



### 1. Zuerst habe ich mit den Angaben von der Anleitung eine neue Launch Templates mit dem Namen KN06_VUK_LaunchTemplate_2 erstellt.


![image](https://github.com/user-attachments/assets/d9f3f693-e136-4ff1-aa5f-2d8b6ffeede4)



---

### 2. Jetzt habe ich eine neue Auto Scaling Group erstellt mit dem Namen KN06_VUK_AutoScalingGroup_2


![image](https://github.com/user-attachments/assets/d4809fc2-d055-4e17-a351-e4624cfda153)


---

### 3. Hier sieht man das die beiden Instancen in einer unterschiedlichen Availability Zones liegen und der Status active ist.


![image](https://github.com/user-attachments/assets/07f8d307-c8a9-4b50-a4ea-720c3e360451)



---
### 4. Jetzt sieht man auch die ID der jeweiligen Instance.

![image](https://github.com/user-attachments/assets/aa78683f-b11f-41c5-9d3b-8cb68609af8e)

![image](https://github.com/user-attachments/assets/5a083569-dd71-41f3-a0ee-2378d3cbdc3e)


---

### 5. Nun musste ich die Target Group erstellen.

#### In diesem Bild sieht man das ich die beiden Instancen hinzugefügt habe:

![image](https://github.com/user-attachments/assets/970b0941-dd49-4764-8a12-8daf5281b195)

#### Hier sieht man das er noch keine Zuordnung hat vom Load Balancer dies müssen wir noch machen:

![image](https://github.com/user-attachments/assets/b0470867-c790-47ee-a220-ecf6b21c2196)


---

### 6. In diesem Schritt musste ich einen neuen Load Balancer erstellen mit dem namen KN06-VUK-ALB2.

![image](https://github.com/user-attachments/assets/664766bf-5f04-42a3-8391-177ed345c884)



---

### 7. Jetzt musste ich den Auto Scaling Group der Target Group des Load Balancer zuweisen


![image](https://github.com/user-attachments/assets/fbb482bb-8df9-41bb-83b0-57a7235703bc)


---

### 8. Nun einen Dynamic Scaling policy erzeugen und einbinden

#### Die 20 im Feld Target value ist wie viele Anzahl Reloads gemacht werden müssen bis der Trigger ausgelöst wird:

![image](https://github.com/user-attachments/assets/05211d75-c79d-4da7-952b-2e2165c45014)

#### Hier der Fertig erstellte Dynamic Scaling policy:

![image](https://github.com/user-attachments/assets/0655b57d-71fc-4675-931a-e905d049f1ed)


---

### 9. Beweis Bilder von den Instancen





---

### Fazit


