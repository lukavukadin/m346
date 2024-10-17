# Dokumentation: Instanz mit Cloud-Init deployen

## 1. Cloud-Init Config Datei

Für die Erstellung der Instanz haben wir eine Cloud-Init Konfigurationsdatei verwendet. Diese Datei ist im Repository abgelegt und enthält die notwendigen Einstellungen für den Zugriff über SSH.

### Beispiel der Cloud-Init Datei

```yaml
#cloud-config
users:
  - name: ubuntu
    sudo: ALL=(ALL) NOPASSWD:ALL
    groups: users, admin
    home: /home/ubuntu
    shell: /bin/bash
    ssh-authorized-keys:
      - ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDhQ8vwJIRsyfGmiAMOVHa5zewH0QzAcgDTmuy5Xi+VL93iJzep7PaalZ9eWLqiMn+r2XQ6yddldnwhl6fswq6vpgDw4QZFvuT0azGwcOF0LMWzikuIj9G/spAutVubwFyivY46msuloGVn3fFY+Q6YsiIQCvLLrJQFE1ZAvF+lqGgW6V24Wo40WpEU+0m2EaU4VSbqmGegHSkEGl7lT4orwzQ/BgFmAFB+yyyzPQkYl1OVSO1JHAkWdj5g+ESWg8K7p9OgIut608C8KybwaSxCLQy9D4dFZVZJBROx172LvPcUVJ5n1cZ1B9ZfKx42YHo52wJCX6RLJd1DwUbY51eF lukas

ssh_pwauth: false
disable_root: false
package_update: true
packages:
  - curl
  - wget

```

## 2. Verwendete Key

Beim Start der Instanz wurde der Schlüssel Luka-2.pem verwendet. In der Cloud-Init Datei ist der Public Key von Luka-1.pem als autorisierter Schlüssel angegeben.

![image](https://github.com/user-attachments/assets/e2e8d3d0-0225-4264-8789-560147ea9160)


## 3. SSH Login mit erstem Key

Der Zugriff mit dem ersten Schlüssel Luka-1.pem gelingt erfolgreich, da dieser in der Cloud-Init Datei als autorisierter Schlüssel definiert wurde.

![image](https://github.com/user-attachments/assets/87ffab87-ea71-4611-a2c0-a106cda8e43c)

## 4. SSH Login mit zweitem Key

Der Zugriff mit dem zwetien Schlüssel Luka-2.pem schlägt fehl, weil der zweite Schlüssel von der Cloud-Init Config überschrieben wurde.

![image](https://github.com/user-attachments/assets/94cf2cb6-e221-415d-b465-83543487f2b8)


## 5. Cloud-Init Output Log

Im Cloud-Init Output Log kann man erkennen, dass die Konfiguration erfolgreich war. Es wurden die notwendigen Software-Pakete, wie wget und curl, installiert, was bedeutet, dass die Konfiguration vollständig erfolgreich war.

![image](https://github.com/user-attachments/assets/c9a3fd26-c5ff-4286-abd8-a402be392e9e)



## 6. Überprüfen der Installation 

Hier in diesem Screenshot sieht man die erfolgreiche Installation von curl und wget 

![image](https://github.com/user-attachments/assets/97608bd2-f786-4f8b-9775-53868228df94)

