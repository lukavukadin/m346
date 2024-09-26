# AWS Speicherdienste

## 1. AWS Speicherdienste

### a. Amazon EBS (Elastic Block Store)
- **Einsatzbereich:** Blockspeicher für EC2-Instanzen.
- **Beispiele:**
  - Datenbanken (z.B. MySQL)
  - Anwendungen mit hoher IOPS-Anforderung.

### b. Amazon S3 (Simple Storage Service)
- **Einsatzbereich:** Objektbasierter Speicher für unstrukturierte Daten.
- **Beispiele:**
  - Medieninhalte (Bilder, Videos)
  - Backup- und Archivierungslösungen.

### c. Amazon EFS (Elastic File System)
- **Einsatzbereich:** Gemeinsames Dateisystem für EC2-Instanzen.
- **Beispiele:**
  - Webanwendungen mit gemeinsam genutzten Dateien.
  - Content-Management-Systeme.

## 2. Persistenter vs. Flüchtiger Speicher

- **Persistenter Speicher:**
  - Daten bleiben nach Instanz-Stopps erhalten (z.B. EBS, S3).
  - **Beispiel:** EBS-Datenbank speichert Daten nach Neustart.

- **Flüchtiger Speicher:**
  - Daten gehen bei Instanz-Stopps verloren (z.B. Instance Store).
  - **Beispiel:** Temporäre Dateien in Instance Store.

## 3. Unterschiede in den Geschwindigkeiten

- **EBS:** Hohe IOPS und niedrige Latenz (SSD vs. HDD).
- **S3:** Optimiert für Skalierbarkeit, aber langsamer (Millisekunden).
- **EFS:** Gute Leistung mit niedriger Latenz, aber langsamer als EBS-SSD.

