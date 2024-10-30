# EBS Volume erstellen, Snapshot ziehen und daraus neues Volume erzeugen

### 1. Zuerst habe ich ein Volumes erstellt mit den Angaben von der Anleitung


![image](https://github.com/user-attachments/assets/3179d2ce-babb-4f64-8e35-e2680467e604)



---

### 2. Nun habe ich am erstellten Volumen die Instance "Lab" angehängt


![image](https://github.com/user-attachments/assets/4b8b2f16-3849-42ed-8067-5815cb899200)


---

### 3. Jetzt habe ich eine Verbindung mit meiner Instance hergestellt

![image](https://github.com/user-attachments/assets/c6ab38a4-fdfe-4ba4-bcb1-794d80ae557b)



---

### 4. In diesem Schritt habe ich ein Dateisystem erstellt und konfiguriert

![image](https://github.com/user-attachments/assets/5f17dc08-f637-4e8f-8694-2916d7a25fe1)

**Zeigt den verfügbaren und verwendeten Speicherplatz aller gemounteten Partitionen an:**
```
df -h
```

**Formatiert das Gerät /dev/sdf mit dem Dateisystem ext3:**
```
sudo mkfs -t ext3 /dev/sdf
```

**Erstellt ein Verzeichnis namens "data-store" unter /mnt, um es als Mount-Punkt zu verwenden:**
```
sudo mkdir /mnt/data-store
```

**Mountet das Gerät /dev/sdf im Verzeichnis /mnt/data-store mit ext3-Dateisystem und bestimmten Mount-Optionen (defaults, noatime). Fügt diese Konfiguration in /etc/fstab hinzu, damit das Laufwerk beim Systemstart automatisch gemountet wird:**
```
echo "sudo mount /dev/sdf /mnt/data-store ext3 defaults,noatime 1 2" | sudo tee -a /etc/fstab
```

**Zeigt den Inhalt der Datei /etc/fstab an, um die neuen Mount-Einstellungen zu überprüfen:**
```
cat /etc/fstab
```

**Schreibt den Text "some text has been written" in eine neue Datei namens file.txt im Verzeichnis /mnt/data-store:**
```
sudo sh -c "echo some text has been written > /mnt/data-store/file.txt"
```

**Zeigt den Inhalt der Datei /mnt/data-store/file.txt an, um die geschriebenen Daten zu überprüfen:**
```
cat /mnt/data-store/file.txt
```


---

### 5. Nun habe ich einen Snapshot erstellt

#### Hier sieht man den erfolgreichen Snapshot von der Instance:

![image](https://github.com/user-attachments/assets/5e466c76-269e-42c9-8170-6cb5bf157b32)

#### Jetzt muss ich das File was ich im vorherigem Schritt erstellt habe löschen:

![image](https://github.com/user-attachments/assets/7c17cab7-bded-4fbf-beb3-69fe8914a546)



---

### 6. Wiederherstellen des EBS-Snapshots

#### In diesem Schritt habe ich ein neues Volumen erstellt mit der gleichen Availability Zone us-east-1a, einfach mit einem anderen Wert "Restored Volume":

![image](https://github.com/user-attachments/assets/2e2cc61a-918c-4b52-ad89-ddfc490c104f)

#### Ich habe jetzt das Volumen an meine Instance eingefügt:

![image](https://github.com/user-attachments/assets/ea26d787-0eab-4632-a8aa-49c3830c0f89)

#### Jetzt muss ich das Restored Volume mounten:

![image](https://github.com/user-attachments/assets/6d857ccd-59b4-40f9-b22b-4d2271f13713)

---

### 7. Hier sieht man die Volle Punktzahl der Aufgabe

![image](https://github.com/user-attachments/assets/6de466b6-bf54-42ab-8c6e-fc901e6dbbe1)

---

### Fazit

Ich hatte keine Probleme, und alles ging reibungslos. Die Schritte zum Erstellen des EBS-Volumes, Anhängen an die EC2-Instance, Erstellen des Dateisystems, Erstellen des Snapshots und Wiederherstellen des Volumes wurden ohne Komplikationen erfolgreich abgeschlossen. Das gesamte Verfahren verlief effizient, und ich konnte die volle Punktzahl für die Aufgabe erreichen.


