## Servicemodelle


### Die vier Servicemodelle

#### IaaS (Infrastructure as a Service)
- **Definition:** Bereitstellung von virtuellen Infrastruktur-Ressourcen wie Servern, Speicher und Netzwerken.
- **Beispiel:** Amazon Web Services (AWS), Microsoft Azure.
- **Pizza-Prinzip:** Wie das Kaufen von Zutaten und das Backen der Pizza zu Hause. Sie kontrollieren die gesamte Zubereitung, müssen aber alles selbst erledigen.

#### PaaS (Platform as a Service)
- **Definition:** Bereitstellung einer kompletten Plattform, die Entwicklungsumgebungen und Laufzeitumgebungen umfasst, um Anwendungen zu entwickeln und zu betreiben, ohne sich um die zugrunde liegende Infrastruktur kümmern zu müssen.
- **Beispiel:** Heroku, Google App Engine.
- **Pizza-Prinzip:** Wie der Erhalt eines vorgefertigten Pizzateigs und Belägen im Pizzarestaurant. Sie gestalten Ihre Pizza, ohne sich um die Basis kümmern zu müssen.

#### SaaS (Software as a Service)
- **Definition:** Bereitstellung von vollständigen Softwareanwendungen über das Internet. Die Nutzer greifen über Webbrowser oder APIs auf die Anwendungen zu.
- **Beispiel:** Office 365, Slack, Dropbox.
- **Pizza-Prinzip:** Wie das Bestellen einer fertigen Pizza bei einem Lieferdienst. Sie nutzen die fertige Anwendung, ohne sich um die Installation oder Wartung kümmern zu müssen.

#### FaaS (Function as a Service)
- **Definition:** Bereitstellung von Funktionen als Service, bei dem nur die Geschäftslogik implementiert werden muss, während die Infrastruktur und Plattform vom Anbieter verwaltet werden.
- **Beispiel:** AWS Lambda, Azure Functions.
- **Pizza-Prinzip:** Wie das Ergänzen von Funktionen zu einem bereits bestehenden Anwendungsrahmen. Die gesamte Infrastruktur wird vom Anbieter bereitgestellt.


### Hierarchie der Servicemodelle

- **IaaS** ist die Grundlage, auf der **PaaS** aufbaut. IaaS stellt die grundlegende Infrastruktur bereit, auf der PaaS-Anbieter ihre Plattformen aufbauen.
- **PaaS** baut auf **IaaS** auf, indem es zusätzlich zur Infrastruktur auch eine Entwicklungsplattform bereitstellt.
- **SaaS** baut auf **IaaS** und **PaaS** auf, indem es fertige Softwarelösungen zur Nutzung anbietet, die auf den zugrunde liegenden IaaS- und PaaS-Ressourcen laufen.
- **FaaS** ist eine spezielle Form, die auf den grundlegenden Modellen aufbauen kann, indem es Funktionen als Service anbietet, oft innerhalb von PaaS- oder IaaS-Umgebungen.


### Beispielprodukte für die Servicemodelle

- **IaaS:** Amazon Web Services (AWS), Microsoft Azure, Google Cloud Platform, Digital Ocean.
- **PaaS:** Heroku, Google App Engine, AWS Elastic Beanstalk, Microsoft Azure App Services.
- **SaaS:** Office 365, Slack, Dropbox, GitHub.
- **FaaS:** AWS Lambda, Azure Functions, Google Cloud Functions.
