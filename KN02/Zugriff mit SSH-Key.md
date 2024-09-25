## EC2-Instanz mit SSH Key-Authentifizierung

Im Folgenden sind die drei wichtigen Schritte zur Erstellung und Authentifizierung mit SSH-Key-Pairs bei einer EC2-Instanz zusammengefasst:

### 1. Erfolgreicher SSH-Login mit dem ersten Key (`Luka-1.pem`)

Im ersten Schritt habe ich mich erfolgreich mit dem Key-Pair **Luka-1.pem** auf der EC2-Instanz eingeloggt. Auf dem Bild ist der erfolgreiche Login zu sehen.

<img src="https://github.com/user-attachments/assets/37110c76-5c68-4e15-83d3-b370c5bd27ee" alt="Erfolgreicher Login" width="80%"/>

### 2. Fehlgeschlagener SSH-Login mit dem zweiten Key (`Luka-2.pem`)

Der nächste Schritt zeigt den Versuch, sich mit dem zweiten Key-Pair **Luka-2.pem** anzumelden. Dieser Login ist jedoch fehlgeschlagen, da der zugehörige öffentliche Schlüssel nicht auf der EC2-Instanz hinterlegt wurde.

<img src="https://github.com/user-attachments/assets/84c0633c-df49-4dc2-a4a9-fc2972734f0d" alt="Fehlgeschlagener Login" width="80%"/>

### 3. Übersicht der EC2-Instanz und zugewiesener Key-Pair (`Luka-1.pem`)

Zum Abschluss habe ich eine Übersicht der erstellten EC2-Instanz aufgenommen. Diese zeigt, dass der Key-Pair **Luka-1.pem** der Instanz zugewiesen wurde.

<img src="https://github.com/user-attachments/assets/38612311-7f29-4c54-8c39-a2a935e66359" alt="EC2-Instanz Übersicht" width="80%"/>


