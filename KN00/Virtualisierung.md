# Virtualisierung

## 1. Begriff der Virtualisierung
- **Definition:** Virtualisierung bezeichnet den Prozess, bei dem physische Ressourcen (wie Server, Speicher oder Netzwerke) in virtuelle Ressourcen umgewandelt werden. Dies ermöglicht die gleichzeitige Ausführung mehrerer Betriebssysteme oder Anwendungen auf einer einzigen Hardware-Plattform.

## 2. Rolle des Hypervisors
- **Definition:** Ein Hypervisor ist eine Software-Schicht, die es ermöglicht, mehrere virtuelle Maschinen (VMs) auf einer physischen Hardware zu erstellen und zu verwalten. Er agiert als Vermittler zwischen den VMs und der physischen Hardware.
- **Aufgaben:**
  - Zuweisung von Ressourcen (CPU, RAM, Speicher) an die VMs.
  - Verwaltung der Isolation und Sicherheit zwischen den VMs.

## 3. Typen von Hypervisors

### a. Typ 1 Hypervisor (Bare-Metal)
- **Definition:** Ein Typ 1 Hypervisor läuft direkt auf der physischen Hardware, ohne ein darunter liegendes Betriebssystem.
- **Beispiele:** VMware vSphere, Microsoft Hyper-V, Xen.
- **Vorteile:**
  - Höhere Leistung und Effizienz.
  - Bessere Sicherheit, da weniger Angriffsvektoren vorhanden sind.

### b. Typ 2 Hypervisor (Hosted)
- **Definition:** Ein Typ 2 Hypervisor läuft auf einem bestehenden Betriebssystem (Host-Betriebssystem).
- **Beispiele:** VMware Workstation, Oracle VirtualBox.
- **Vorteile:**
  - Einfachere Installation und Verwendung.
  - Ideal für Entwicklungs- und Testumgebungen.

## 4. Begriff "Hyperscaler"
- **Definition:** Hyperscaler sind Unternehmen, die große Rechenzentren und Cloud-Infrastrukturen betreiben, um enorme Mengen an Daten zu verarbeiten und zu speichern. Sie bieten skalierbare Cloud-Dienste für Unternehmen und Endbenutzer.
- **Beispiele:** Amazon Web Services (AWS), Microsoft Azure, Google Cloud Platform (GCP).

## 5. Schichten von Cloud-Systemen
- **Infrastruktur (IaaS):** Bereitstellung von virtualisierten Hardware-Ressourcen (z.B. Server, Storage) über das Internet.
- **Plattform (PaaS):** Bereitstellung von Entwicklungs- und Bereitstellungsumgebungen, die es Entwicklern ermöglichen, Anwendungen ohne sich um die zugrunde liegende Infrastruktur zu kümmern, zu erstellen.
- **Software (SaaS):** Bereitstellung von Software-Anwendungen über das Internet, die von den Benutzern abgerufen und genutzt werden, ohne dass eine lokale Installation erforderlich ist.

