# VPC mit je zwei Pulbic- und Private Subnets in zwei verschiedenen AZ erstellen

### 1. Als erstes habe ich eine VPC erstellt mit diesen Angaben:

Name: M346-VUK-VPC
IPv4 CIDR Block: 10.0.0.0/16


### 2. Als nächstes die Subnets erstellen:

**1. Subnetz**
   
Name: M346-VUK-Public-1A
Availability Zone: us-east-1a
IPv4 CIDR Block: 10.0.1.0/24

**2. Subnetz**
   
Name: M346-VUK-Public-1B
Availability Zone: us-east-1b
IPv4 CIDR Block: 10.0.2.0/24

**3. Subnetz**
Name: M346-VUK-Private-1A
Availability Zone: us-east-1a
IPv4 CIDR Block: 10.0.3.0/24

**4. Subnetz**

Name: M346-VUK-Private-1B
Availability Zone: us-east-1b
IPv4 CIDR Block: 10.0.4.0/24

### 3. Als nächstes habe ich den Public und Private route Tabelle erstellt:

**Public route table (Main)**

Beim Erstellen der VPC wird diese automatisch erzeugt. Es muss einfach folgendes Feld ergänzt werden:
Name: M346-VUK-Public-RT

**Create private route table**

Name: M346-VUK-Private-RT
VPC: M346-VUK-VPC
Subnet associations: Private-1A, Private-1B


### Zum Schluss habe ich noch das Internet Gateway:

Name: M346-VUK-IGW
VPC: M346-VUK-VP


## Erstellte M346-VUK-VPC

In diesem Bild sieht man die Übersicht meiner erstellten VPC. Mithilfe der Schritt-für-Schritt-Anleitung von Herrn Calisto in Gitlab habe ich die VPC erfolgreich konfiguriert. Dabei bin ich sorgfältig vorgegangen und habe jeden Schritt genau nachvollzogen, um sicherzustellen, dass ich die einzelnen Komponenten und deren Zweck vollständig verstehe.

Die Anleitung war klar strukturiert, was mir dabei geholfen hat, die VPC gemäß den Anforderungen zu erstellen und die notwendigen Ressourcen richtig zu konfigurieren.

![image](https://github.com/user-attachments/assets/e8407934-10c4-4c40-b95b-057e02fc35e2)

