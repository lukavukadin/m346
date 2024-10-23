## Zwei Linux Instanzen aufsetzen. 1x im Public- und 1x im Private Subnet in der vorher erstellten VPC.md


1. Die zwei Sicherheitsgruppen erstellt

![image](https://github.com/user-attachments/assets/a4c90f2d-a95c-40d3-956a-f90e3d3aff9b)


2. Jetzt habe ich einen neuen Key pair erstellt

![image](https://github.com/user-attachments/assets/a98d2b4f-aa0a-4ed4-a723-525ded2bd180)



3. Hier sind die zwei Instancen die ich erstellt habe.

![image](https://github.com/user-attachments/assets/e2a600b2-52f0-4e19-8195-e1d98e9e6aa8)



4. Hier sieht man genauere Details von meiner Private Instance; Keine Öffnetliche IP wie es sein muss, aber es hat eine Private IP die mit 10.0.4. anfängt.

![image](https://github.com/user-attachments/assets/baf395ee-1939-434b-86f6-105bf427e7f4)



5. Hier sieht man genauere Details von meiner Webserver Instance; Eine Öffnetliche IP wie es sein muss und sie fängt an mit 10.0.1.

![image](https://github.com/user-attachments/assets/a9c79fa3-2700-4146-b77b-7b1feb657b1f)


6. Test ausführungen

Zuerst habe ich getstet ob der Webserver mit meiner Öffenlichen Ip "http://18.234.159.209/" funktioniert und er hat funktioniert sieht man im Bild unten. Am Anfang hat es nicht funktioniert und ich musste dann Änderungen vornehmen.

![image](https://github.com/user-attachments/assets/bbca4b2c-3fdc-4ac2-8e52-1dada5110242)


Dann habe ich getestet ob der SSH Zugriff funktioniert der hat auch funktioniert.

![image](https://github.com/user-attachments/assets/a7722169-2aa0-46df-8f5d-bff1f5fe89c3)


Zum Schluss habe ich auch noch getestet, ob der Ping erfolgreich funktioniert. Und es hat nicht funktioniert.

