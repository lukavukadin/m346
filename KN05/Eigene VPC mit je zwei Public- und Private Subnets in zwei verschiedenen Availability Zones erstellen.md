# VPC mit je zwei Pulbic- und Private Subnets in zwei verschiedenen AZ erstellen

## Namensgebung

### Create VPC

Name: M346-VUK-VPC
IPv4 CIDR Block: 10.0.0.0/16

### Create Public Subnets

Name: M346-VUK-Public-1A
Availability Zone: us-east-1a
IPv4 CIDR Block: 10.0.1.0/24

Name: M346-VUK-Public-1B
Availability Zone: us-east-1b
IPv4 CIDR Block: 10.0.2.0/24

Name: M346-VUK-Private-1A
Availability Zone: us-east-1a
IPv4 CIDR Block: 10.0.3.0/24

Name: M346-VUK-Private-1B
Availability Zone: us-east-1b
IPv4 CIDR Block: 10.0.4.0/24

Public route table (Main)
Beim Erstellen der VPC wird diese automatisch erzeugt. Es muss einfach folgendes Feld ergänzt werden:
Name: M346-VUK-Public-RT

### Create private route table
Name: M346-VUK-Private-RT
VPC: M346-VUK-VPC
Subnet associations: Private-1A, Private-1B

### Create Internet Gateway
Name: M346-VUK-IGW
VPC: M346-VUK-VP
