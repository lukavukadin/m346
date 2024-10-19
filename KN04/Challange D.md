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

### Fazit

Als Einsteiger im Bereich der AWS-Speicherdienste ist es entscheidend, die Stärken und Schwächen der verschiedenen Speicherlösungen zu verstehen. EBS bietet hohe Leistung und Persistenz, ideal für datenintensive Anwendungen, die niedrige Latenz benötigen. S3 ist flexibler und eignet sich besonders für Backups und Datenarchivierung mit globalem Zugriff, während EFS eine gute Wahl für gemeinsam genutzte Dateisysteme ist, insbesondere bei verteilten Anwendungen oder Big Data-Workloads.

Durch dieses Wissen kann ich nun fundierter entscheiden, welche Lösung für unterschiedliche Anforderungen am besten geeignet ist.
