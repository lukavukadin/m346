# Modul 2: Strukturen der Cloud


**1. Wie erhält Ihr Computer Informationen aus dem Internet? Wenn Sie eine Website öffnen, woher kommt die Website? Wer stellt die Daten zur Verfügung? Nutzen Sie in Ihrer Antwort, was Sie über Informatik und Cloud Computing gelernt haben."**

- Wenn ich eine Website öffne, kommen die Informationen von einem Server, der die Seite im Internet bereitstellt. Der Server sendet die Daten an meinen Computer, damit die Website angezeigt werden kann.

**2. Was ist ein Programm oder eine App, die Sie verwenden und die vollständig in der Cloud läuft, sodass Sie nichts auf Ihrem Computer oder Gerät speichern müssen? Wozu nutzen Sie das Programm? Wie wird Ihnen das Programm Ihrer Meinung nach zu geringen oder keinen Kosten zur Verfügung gestellt?**

- Ich nutze Canva und ChatGPT, beide laufen vollständig in der Cloud und ich verwende sie hauptsächlich für schulische Aufgaben. Sie sind kostenlos zugänglich, weil sie auf einem Freemium-Modell basieren, bei dem Basisfunktionen gratis sind und erweiterte Funktionen kostenpflichtig.

**3. Immer mehr Programme und Apps werden von der lokalen Speicherung auf einzelnen Computern in die Cloud verlagert. Beispielsweise nutzen viele Menschen inzwischen internetbasierte Textverarbeitungsprogramme anstelle von Software wie Microsoft Word und Spotify anstelle von CDs und MP3-Playern. Welches weitere Programm oder welcher Dienst wird Ihrer Meinung nach in die Cloud verlagert? Warum bewegt sich Ihrer Meinung nach die Technologie in Richtung Cloud Computing? Begründen Sie Ihre Ideen auf der Grundlage dessen, was Sie zuvor über Cloud Computing gelernt haben.**

- Ein  Beispiel für die Verlagerung in die Cloud ist Spiele-Streaming. Dienste wie Google Stadia ermöglichen es Nutzern, anspruchsvolle Spiele direkt über die Cloud zu spielen, ohne teure Hardware zu benötigen, was den Zugang zu hochwertigen Spielen erheblich vereinfacht. Die Verlagerung von Diensten in die Cloud ermöglicht schnellen, ortsunabhängigen Zugriff und reduziert den Bedarf an lokaler Speicherung und Kabelmanagement. Dadurch wird die Nutzung flexibler und effizienter, da man nicht mehr vor Ort sein muss.


--- 

## Aktivität 1: Visualisierung der AWS Global Infrastructure

### Ziele

- Erkläre den Zweck einer Region, Verfügbarkeitszone und Edge-Standorte.
- Identifiziere die Verbindungen zwischen Regionen, Verfügbarkeitszonen und Edge-Standorten.

### Übersicht

In dieser Aktivität lernst du über die AWS-Infrastruktur und deren Zweck. Du wirst Notizen darüber machen, was Regionen, Verfügbarkeitszonen und Edge-Standorte sind und wofür sie verwendet werden. Außerdem wirst du deine eigenen Diagramme der AWS-Infrastruktur erstellen, um dir das Konzept besser einzuprägen.

#### Region
Eine Region ist ein geografischer Bereich, in dem Daten gespeichert werden. Die Speicherung von Daten in einer Region, die dir am nächsten ist, ermöglicht den schnellen Zugriff auf diese Daten.

#### Verfügbarkeitszone
Eine Verfügbarkeitszone ist ein Rechenzentrum, das viele Server beherbergt. Jede Region hat mehrere isolierte Standorte, die als Verfügbarkeitszonen bekannt sind. Die Verfügbarkeitszonen einer Region sind durch latenzarme Verbindungen miteinander verbunden. Eine Verfügbarkeitszone wird durch einen Regionscode gefolgt von einem Buchstaben identifiziert, zum Beispiel `us-east-1a`.

#### Edge-Standort
Ein Edge-Standort ist ein Standort, an dem Daten für geringere Latenz gespeichert werden können. Oft befinden sich Edge-Standorte in der Nähe von stark bevölkerten Gebieten, die ein hohes Verkehrsaufkommen erzeugen.

#### Aktivitätsanweisungen

Befolge die Anweisungen deines Lehrers, um die Aktivität abzuschließen. Hier sind einige Webseiten, die dir bei dieser Aktivität helfen könnten:

- [Regions and Availability Zones](https://aws.amazon.com/de/about-aws/global-infrastructure/regional-product-services/)
- [AWS Global Infrastructure](https://aws.amazon.com/de/about-aws/global-infrastructure/)
- [AWS Global Cloud Infrastructure](https://aws.amazon.com/de/about-aws/global-infrastructure/cloud/)

### Reflexion

Nachdem du die Aktivität abgeschlossen hast, sei bereit, diese Fragen zu beantworten und zu diskutieren:

1. Vergleiche dein Diagramm mit dem eines anderen Schülers. Gibt es Unterschiede? Was ist gleich?
2. Wie sind Regionen, Verfügbarkeitszonen und Edge-Standorte miteinander verbunden?

---


## Aktivität 2: Arten von Cloud-Diensten

### Ziele

- Erkenne die Arten des Cloud-Computings.
- Vergleiche die Arten des Cloud-Computings.

## Übersicht

In dieser Aktivität lernst du die drei verschiedenen Arten von Cloud-Diensten kennen. Wir werden die Vorteile der Nutzung dieser Cloud-Dienste im Vergleich zu traditionellen Modellen besprechen.

## Aktivitätsanweisungen

Befolge die Anweisungen deines Lehrers, um die Aktivität abzuschließen.

## Reflexion

Nachdem du die Aktivität abgeschlossen hast, sei bereit, diese Frage zu beantworten und zu diskutieren:

Eine Kinderärztin mit einer Privatpraxis hat so viele Patientenakten, dass sie keinen Platz mehr in ihren Aktenschränken hat. Aus diesem Grund möchte sie ihre Daten in die Cloud verlagern. Sie möchte sicherstellen, dass die Daten sicher sind, und möchte, dass ihre Patienten in der Lage sind, ihre medizinischen Unterlagen online sicher zuzugreifen und mit ihr zu kommunizieren. Beschreibe eine Möglichkeit, wie du jeden Typ von Cloud-Service nutzen kannst und wie dies ihrem Geschäft zugutekommen würde.

### Beispielantworten

1. **Infrastructure as a Service (IaaS)**: Die Kinderärztin könnte einen IaaS-Anbieter wie AWS oder Microsoft Azure nutzen, um ihre Serverinfrastruktur in die Cloud zu verlagern. Dadurch könnte sie die Kosten für Hardware reduzieren und ihre Daten sicher speichern, ohne sich um physische Server kümmern zu müssen.

2. **Platform as a Service (PaaS)**: Sie könnte eine PaaS-Lösung wie Google App Engine verwenden, um eine benutzerdefinierte Anwendung zu entwickeln, die es ihren Patienten ermöglicht, sicher auf ihre medizinischen Unterlagen zuzugreifen und mit ihr zu kommunizieren. Das vereinfacht die Entwicklung und Wartung der Anwendung.

3. **Software as a Service (SaaS)**: Die Kinderärztin könnte SaaS-Anwendungen wie einen elektronischen Gesundheitsakten-Dienst (z.B. Practice Fusion oder Athenahealth) nutzen. Diese Dienste bieten bereits sichere und konforme Plattformen, auf denen Patienten ihre Daten verwalten und kommunizieren können, ohne dass die Ärztin sich um die technischen Aspekte kümmern muss.

### Vorteile für ihr Geschäft

Die Verwendung dieser Cloud-Dienste würde der Kinderärztin helfen, ihre Patientenakten sicher und effizient zu verwalten, während sie gleichzeitig den Zugang für ihre Patienten erleichtert. Darüber hinaus könnte sie Zeit und Kosten sparen, indem sie die Notwendigkeit physischer Infrastruktur und Wartung reduziert.


