# Speicherdienste und entsprechende Eigenschaften kennen (Beginner)



| **Eigenschaft**         | **EBS (Elastic Block Store)** | **S3 (Simple Storage Service)** | **EFS (Elastic File System)**   |
|-------------------------|-------------------------------|---------------------------------|---------------------------------|
| **Speichertyp**          | Block Storage                 | Object Storage                  | File Storage                   |
| **Persistenz**           | Ja                            | Ja                              | Ja                              |
| **Geschwindigkeit**      | Sehr hoch                     | Variabel (niedriger als EBS)    | Mittel bis hoch                |
| **Sicherheit**           | Sehr hoch (Verschlüsselung, IAM) | Sehr hoch (Verschlüsselung, IAM, Bucket Policies) | Hoch (Verschlüsselung, IAM) |
| **Standort**             | Regional                      | Global (kann regional begrenzt werden) | Regional                     |
| **Weitere Charakteristiken** | Gebunden an eine EC2-Instanz, geeignet für Datenbanken mit niedriger Latenz | Skalierbare Speicherung für unstrukturierte Daten, unbegrenzte Kapazität | Kann von mehreren EC2-Instanzen gleichzeitig genutzt werden, NFS-kompatibel |
| **Use-case**             | Datenbanken, die niedrige Latenz erfordern | Backups, Archivierung, statische Webseiten, Datenanalysen | Gemeinsame Dateisysteme für Webserver, Big Data-Workloads, Container-Orchestrierung |

----

### Quellen

**ChatGPT** - Erkläre mir die drei Speicherdienste: EBS, S3 und EFS in diesen verschiednenen Kategorien: 

Persistenz (Ja/Nein)
Geschwindigkeit (grobe Unterteilung)
Sicherheit (insbesondere bei Object-Storage)
Standort (Region oder Global)
Weitere Charakteristiken
Use-case (Ein Anwendungsbeispiel für jeden Storage-Typ)
