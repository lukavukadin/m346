# Dokumentation zur SSH-Zugriffsverwaltung auf EC2-Instanz

## Ziel
Das Ziel dieser Aufgabe war es, SSH-Zugriff auf eine EC2-Instanz mit mehreren Schlüsseln zu konfigurieren, um sowohl den Zugriff meines Lehrers als auch meinen eigenen Zugriff sicherzustellen.

## Vorgehensweise

### 1. Erstellen eines neuen SSH-Schlüssels für den Lehrer
- Ich erhielt den öffentlichen SSH-Schlüssel meines Lehrers. Der Schlüssel sieht wie folgt aus:

```
--- BEGIN PUBLIC KEY - CAL ---- AAAAB3NzaC1yc2EAAAADAQABAAACAQCz/wpWmsCxaQyuNFrIachc/q9nUdByoUcBc icl/wnKLFktKp6du9np9Uhmo4M0tVHNnWCt5uNEi2ks/0XEbg2J+4heuAAKEDr/TV bgabiWGclYKpEWZvmw8gsQwfpAKVG4aS2re7wB2uhw82ZqzJVpGm3ne+sNnz5uVrx N8HUnuR2OWJD6bA9l/fBmE6zdObVXgrCJGjZmVyB5GMeTDJKExgoBpLggZn9CNdu7 Sx989xtNLehu6SWM+mGCq9Lcu7usiPG+SuEb8XynYaCOnv8+Oko6SYeJ9Omq/E7Eg 6vZHqCbBQ81TIZrGKcikLmF2xP7EOprGOSPVewke7ak7vvmOI+p/RfIAyXj1+GYny +esk9G+qDRFXP9uiIlMfH1oGkQkztvSDMH+EOHqgY66NWQJPj83CaWH/euR0MROHX jm1ar3RuN9qcASAnzCOQQ1FMwFkpIV5x0NDRx0Zp1rLt8ZUFykmIuHZI4g9u6RdAi uWUxx9/eF0fXZa6Ju7GEMKeMtZxJJjmB/WCOylbkT+NPw5RcxgyRLKmUAicnYKXBm ULY3pQM/Ui8KiCyJqRbLDBAR+XZYsZ7X5uhcuteu8KIfA2xEbInB4Q3c0DnnSih+G EC4pEbz+NOfeCpLJEn4gfyV1S9S08sG62ls8NPFociA9aWmE1oXfcqwvOkkYhxOw== ---- END SSH2 PUBLIC KEY ----
```


### 2. Hinzufügen des öffentlichen Schlüssels zur `authorized_keys`-Datei
- Ich habe den öffentlichen Schlüssel meines Lehrers in die Datei `~/.ssh/authorized_keys` auf der EC2-Instanz eingefügt. Hier sind die Schritte, die ich dafür unternommen habe:

1. **Mit der EC2-Instanz verbinden**:
   ```bash
   ssh -i "C:\Users\vukadinl\Luka-1.pem" ubuntu@54.81.9.226


2. **Öffnen der authorized_keys-Datei:**

```
nano ~/.ssh/authorized_keys
```

3. **Einfügen des öffentlichen Schlüssels:**

Ich habe den Schlüssel in die Datei eingefügt und die Datei gespeichert.

![image](https://github.com/user-attachments/assets/6b993b4d-7061-42e7-bd67-9fa63fc9a11b)



### 3. Sicherstellen, dass ich weiterhin Zugriff habe
Um sicherzustellen, dass ich mich weiterhin mit meinem eigenen Schlüssel (Luka-1.pem) anmelden kann, habe ich die authorized_keys-Datei nicht verändert, die bereits meinen Schlüssel enthielt.


### 4. Überprüfung der Konnektivität
Ich habe versucht, mich mit meinem Schlüssel (Luka-1.pem) anzumelden, um zu bestätigen, dass alles funktioniert:

   
### Fazit
Ich habe erfolgreich den Zugriff auf die EC2-Instanz für meinen Lehrer eingerichtet, während ich gleichzeitig meinen eigenen Zugriff beibehalten habe. Beide Schlüssel sind jetzt in der authorized_keys-Datei vorhanden, was bedeutet, dass sowohl mein Lehrer als auch ich uns anmelden können.
