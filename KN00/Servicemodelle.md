# Servicemodelle

## Die vier Servicemodelle

### IaaS (Infrastructure as a Service)
- **Definition:** Bereitstellung von virtuellen Infrastruktur-Ressourcen wie Servern, Speicher und Netzwerken.
- **Beispiel:** Amazon Web Services (AWS), Microsoft Azure.
- **Pizza-Prinzip:** Wie das Kaufen von Zutaten und das Backen der Pizza zu Hause. Sie kontrollieren die gesamte Zubereitung, müssen aber alles selbst erledigen.

<img src="https://github.com/user-attachments/assets/b5156994-d80d-4ab2-a98d-a00d1ad386e0" alt="IaaS Bild" width="40%" height="auto">

### PaaS (Platform as a Service)
- **Definition:** Bereitstellung einer kompletten Plattform, die Entwicklungsumgebungen und Laufzeitumgebungen umfasst, um Anwendungen zu entwickeln und zu betreiben, ohne sich um die zugrunde liegende Infrastruktur kümmern zu müssen.
- **Beispiel:** Heroku, Google App Engine.
- **Pizza-Prinzip:** Wie der Erhalt eines vorgefertigten Pizzateigs und Belägen im Pizzarestaurant. Sie gestalten Ihre Pizza, ohne sich um die Basis kümmern zu müssen.

<img src="https://github.com/user-attachments/assets/1e6e9222-ecb7-45df-aa34-a713b06749a6" alt="PaaS Bild" width="40%" height="auto">

### SaaS (Software as a Service)
- **Definition:** Bereitstellung von vollständigen Softwareanwendungen über das Internet. Die Nutzer greifen über Webbrowser oder APIs auf die Anwendungen zu.
- **Beispiel:** Office 365, Slack, Dropbox.
- **Pizza-Prinzip:** Wie das Bestellen einer fertigen Pizza bei einem Lieferdienst. Sie nutzen die fertige Anwendung, ohne sich um die Installation oder Wartung kümmern zu müssen.

<img src="https://github.com/user-attachments/assets/ec851c2c-f57b-43e1-9753-bb81be94524c" alt="SaaS Bild" width="40%" height="auto">

### FaaS (Function as a Service)
- **Definition:** Bereitstellung von Funktionen als Service, bei dem nur die Geschäftslogik implementiert werden muss, während die Infrastruktur und Plattform vom Anbieter verwaltet werden.
- **Beispiel:** AWS Lambda, Azure Functions.
- **Pizza-Prinzip:** Wie das Ergänzen von Funktionen zu einem bereits bestehenden Anwendungsrahmen. Die gesamte Infrastruktur wird vom Anbieter bereitgestellt.

<img src="https://github.com/user-attachments/assets/f770a5f7-6ebe-43aa-95e9-a1699f5fd4a3" alt="FaaS Bild" width="40%" height="auto">

## Hierarchie der Servicemodelle

- **IaaS** ist die Grundlage, auf der **PaaS** aufbaut. IaaS stellt die grundlegende Infrastruktur bereit, auf der PaaS-Anbieter ihre Plattformen aufbauen.
- **PaaS** baut auf **IaaS** auf, indem es zusätzlich zur Infrastruktur auch eine Entwicklungsplattform bereitstellt.
- **SaaS** baut auf **IaaS** und **PaaS** auf, indem es fertige Softwarelösungen zur Nutzung anbietet, die auf den zugrunde liegenden IaaS- und PaaS-Ressourcen laufen.
- **FaaS** ist eine spezielle Form, die auf den grundlegenden Modellen aufbauen kann, indem es Funktionen als Service anbietet, oft innerhalb von PaaS- oder IaaS-Umgebungen.
