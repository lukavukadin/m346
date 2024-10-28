# Recherche zu Fachbegriffen
## High Availability (HA)

---

Wenn ein Stromausfall passieren würde, könnte ich mich darauf verlassen, dass eine unterbrechungsfreie Stromversorgung (USV) sofort einspringt und die Systeme stabil hält, bis die Notstromgeneratoren anlaufen. So wäre alles ohne Unterbrechung weiterhin verfügbar, und ich hätte genug Zeit, um die Lage zu checken und gegebenenfalls weitere Schritte einzuleiten. Wenn diese Systeme regelmäßig gewartet wurden, wäre ich sicher, dass sie genau dann bereit sind, wenn ich sie brauche.

Würde hingegen ein Erdbeben eintreten, könnten meine Systeme durch erdbebensichere Racks geschützt sein, sodass die Hardware stabil bleibt. Noch wichtiger wäre aber, dass ich durch die geografische Verteilung meiner Daten und Systeme direkt auf einen anderen Standort umschalten könnte, falls das Hauptrechenzentrum betroffen ist. Und durch die regelmäßigen Cloud-Backups und den bestehenden Notfallplan wäre sichergestellt, dass ich alle Daten und Systeme schnell wiederherstellen kann.

---

## Fault Tolerance (FT)

Fault Tolerance (FT) ist wichtig, um sicherzustellen, dass die IT auch dann funktioniert, wenn mal was ausfällt. Gerade in einem kleinen Serverraum einer Kleinfirma sollte ich sicherstellen, dass wir ein paar grundlegende Redundanzen einbauen, um bei Problemen direkt reagieren zu können. Hier drei Maßnahmen, die ich einführen würde:

1. **Redundante Stromversorgung**  
   Haupt- und Reserveleitungen sorgen dafür, dass die Server auch bei einem Stromausfall weiterlaufen. In der Cloud ist das mit großen, abgesicherten Stromnetzen und Notstromlösungen gewährleistet.

2. **RAID für Festplattenspiegelung**  
   RAID schützt die Daten, indem sie auf mehreren Festplatten gespiegelt werden. Bei Cloud-Providern erfolgt das ebenfalls und zusätzlich auf verteilten Speicherorten.

3. **Standby-Server**  
   Ein Ersatzserver springt sofort ein, wenn der Hauptserver ausfällt. In der Cloud übernehmen das oft automatisch verteilte Systeme in verschiedenen Regionen.


---

## Load Balancer


#### 1. Was ist ein AWS Load Balancer, und welche Hauptfunktionen erfüllt er im Kontext von AWS?

Ein AWS Load Balancer ist wie ein „Türsteher“ für Anfragen – er verteilt alle eingehenden Anfragen automatisch an die verschiedenen Server, um die Last gleichmäßig zu verteilen. Dadurch bleibt die Anwendung stabil und funktioniert auch bei höherem Traffic zuverlässig.

---

#### 2. Welche verschiedenen Typen von AWS Load Balancern stehen zur Verfügung, und wie unterscheiden sie sich hinsichtlich ihrer Anwendungsfälle und Funktionen?

Es gibt drei Haupttypen:

**Application Load Balancer (ALB)**: 

Er ist speziell für Webanwendungen (HTTP und HTTPS) gemacht und kann Anfragen clever nach Inhalt weiterleiten. Zum Beispiel: eine bestimmte URL schickt er an einen speziellen Server.

**Network Load Balancer (NLB)**: 

Dieser ist schnell und perfekt für Situationen, wo hohe Übertragungsraten und kurze Verzögerungen wichtig sind. Ideal für Echtzeit-Anwendungen.

**Gateway Load Balancer (GLB)**: 

Nutzt man oft für Sicherheitsaufgaben, weil er den Datenverkehr filtern und leiten kann, wie es zum Beispiel in Firewall-Lösungen gebraucht wird.

---

#### 3. Wie können Sie den Auto Scaling-Service von AWS mit Load Balancern kombinieren, um die Skalierbarkeit und Verfügbarkeit Ihrer Anwendungen zu verbessern?

Mit Auto Scaling und Load Balancern kann man Server automatisch aufstocken, wenn viele Nutzer die Anwendung gleichzeitig nutzen. Sobald die Nachfrage sinkt, werden ungenutzte Server heruntergefahren. Das bedeutet, die Anwendung ist immer bereit, egal wie groß der Ansturm ist, und es wird nur bezahlt, was wirklich gebraucht wird.

---

#### 4. Welche Sicherheitsmaßnahmen und Best Practices sollten beim Konfigurieren eines AWS Load Balancers beachtet werden, um Angriffe wie DDoS-Attacken zu verhindern?

Um den Load Balancer sicher zu machen, kann man:
   - **AWS Shield und WAF** (Web Application Firewall) einsetzen – die helfen, Bedrohungen zu erkennen und blockieren Angriffe.
   - **HTTPS aktivieren** – so werden alle Daten verschlüsselt übertragen.
   - **Zugriffsregeln und Sicherheitsgruppen** nutzen – damit kann man genau festlegen, welche IP-Adressen Zugriff bekommen.

---

#### 5. Wie kann die Leistung eines AWS Load Balancers überwacht und optimiert werden, um sicherzustellen, dass er den Anforderungen Ihrer Anwendung gerecht wird?

Mit **CloudWatch** lässt sich die Performance eines Load Balancers überwachen. Wichtige Werte sind zum Beispiel die Anzahl der Anfragen, die Reaktionszeit und wie viele gesunde Server verfügbar sind. Wenn etwas nicht passt, kann man dann direkt anpassen, um die Leistung stabil zu halten.


---

## Auto Scaling

#### 1. Was ist AWS Auto Scaling und welche Hauptfunktion erfüllt es?

AWS Auto Scaling passt die Anzahl der Server automatisch an die aktuelle Nachfrage an. Wenn viel los ist, werden mehr Server gestartet; bei weniger Betrieb fährt AWS die Server wieder herunter.

---

#### 2. Welche Arten von Richtlinien können in AWS Auto Scaling verwendet werden?

Es gibt verschiedene Richtlinien, um Auto Scaling zu steuern:
   - **Zielbasiert** (Target Tracking): AWS skaliert automatisch, um eine bestimmte Auslastung (z.B. CPU) zu halten.
   - **Schwellenwertbasiert** (Step Scaling): Startet zusätzliche Server, wenn ein bestimmter Wert überschritten wird.
   - **Geplantes Scaling**: Automatische Anpassungen basierend auf einer festgelegten Zeit, z. B. zu Stoßzeiten.

---

#### 3. Wie kann die Auto Scaling-Gruppe wissen, wann sie zusätzliche Instanzen starten oder beenden sollte?

Auto Scaling nutzt Alarme (z.B. CPU-Auslastung) von **CloudWatch**, um festzustellen, wann es mehr Server braucht oder welche abgeschaltet werden können, wenn weniger los ist.

---

#### 4. Warum ist AWS Auto Scaling nützlich für die Kostenoptimierung?

Auto Scaling hilft, Kosten zu sparen, indem es nur dann zusätzliche Server startet, wenn sie wirklich gebraucht werden. Das heißt, man zahlt nur für die Serverkapazität, die tatsächlich genutzt wird.

---

#### 5. Welche Rolle spielt die Elastic Load Balancing (ELB) in Verbindung mit AWS Auto Scaling?

Die ELB verteilt automatisch die Anfragen auf die verfügbaren Server. Wenn durch Auto Scaling neue Server hinzukommen, teilt die ELB die Last sofort auf diese auf, sodass alle Server gleichmäßig ausgelastet sind.

---

