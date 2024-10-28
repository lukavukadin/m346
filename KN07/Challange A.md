#  Recherche Datensicherung

### Datensicherung in AWS

**Datensicherung** ist ein Schlüsselthema für jede IT-Infrastruktur, besonders in der Cloud. Amazon Web Services (AWS) stellt verschiedene Tools bereit, um Daten sicher zu speichern und bei Bedarf wiederherzustellen. Zwei zentrale Konzepte dabei sind **Snapshots** und **Backups**.

- **Snapshots**: Schnappschüsse eines EBS-Volumes, die den Zustand zu einem bestimmten Zeitpunkt festhalten. Sie sind effizient, da sie nur Änderungen seit dem letzten Snapshot speichern.
- **Backups**: Umfassendere Sicherungen, die nicht nur den Datenstand, sondern auch Einstellungen und Konfigurationen (z.B. bei EC2-Instanzen, Datenbanken und S3-Buckets) erfassen. Mit dem **AWS Backup**-Dienst können diese Backups zentral verwaltet werden.

---


### EBS Volume erstellen, Snapshot ziehen und daraus neues Volume erzeugen



### Webserver erstellen, Snapshot ziehen und daraus neues Volume erzeugen
