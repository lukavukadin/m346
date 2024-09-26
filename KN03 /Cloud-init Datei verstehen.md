# Cloud-init Datei verstehen

**1. Erklären Sie alle Zeilen der Cloud-init Datei in folgendem Schema.**


```
#cloud-config
users:
  - name: ubuntu
    sudo: ALL=(ALL) NOPASSWD:ALL
    groups: users, admin
    home: /home/ubuntu
    shell: /bin/bash
    ssh_authorized_keys:
      - ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQC0WGP1EZykEtv5YGC9nMiPFW3U3DmZNzKFO5nEu6uozEHh4jLZzPNHSrfFTuQ2GnRDSt+XbOtTLdcj26+iPNiFoFha42aCIzYjt6V8Z+SQ9pzF4jPPzxwXfDdkEWylgoNnZ+4MG1lNFqa8aO7F62tX0Yj5khjC0Bs7Mb2cHLx1XZaxJV6qSaulDuBbLYe8QUZXkMc7wmob3PM0kflfolR3LE7LResIHWa4j4FL6r5cQmFlDU2BDPpKMFMGUfRSFiUtaWBNXFOWHQBC2+uKmuMPYP4vJC9sBgqMvPN/X2KyemqdMvdKXnCfrzadHuSSJYEzD64Cve5Zl9yVvY4AqyBD aws-key       
ssh_pwauth: false
disable_root: false 
package_update: true
packages:
  - curl 
  - wget 
```


Dies ist ein Kommentar, der angibt, dass der folgende Inhalt eine Cloud-init Konfiguration im YAML-Format ist:

```
#cloud-config
```

Beginnt den Block für die Definition von Benutzern, die auf der Instanz erstellt werden sollen:

```
users:
```

Erstellt einen Benutzer mit dem Namen ubuntu. Das Minuszeichen - zeigt an, dass dies eine Liste von Benutzern ist:

```
- name: ubuntu
```

Der Benutzer ubuntu hat die Berechtigung, alle Befehle mit sudo auszuführen, ohne ein Passwort eingeben zu müssen:

```
    sudo: ALL=(ALL) NOPASSWD:ALL
```

Der Benutzer wird den Gruppen users und admin hinzugefügt, was ihm bestimmte Berechtigungen innerhalb des Systems gibt:

```
    groups: users, admin
```

Legt das Home-Verzeichnis des Benutzers ubuntu auf /home/ubuntu fest:

```
    home: /home/ubuntu
```


Setzt die Standard-Shell des Benutzers auf /bin/bash, was bedeutet, dass er die Bash-Shell verwendet, wenn er sich anmeldet:

```
    shell: /bin/bash
```


ssh_authorized_keys: Beginnt den Block für die autorisierten SSH-Schlüssel, die dem Benutzer den Zugriff ermöglichen:

```
    ssh_authorized_keys:
```


Fügt einen autorisierten SSH-Schlüssel hinzu, der es dem Benutzer ermöglicht, sich über SSH ohne Passwort einzuloggen. Der Schlüssel muss in einer einzigen Zeile eingegeben werden:

```
      - ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQC0WGP1EZykEtv5YGC9nMiPFW3U3DmZNzKFO5nEu6uozEHh4jLZzPNHSrfFTuQ2GnRDSt+XbOtTLdcj26+iPNiFoFha42aCIzYjt6V8Z+SQ9pzF4jPPzxwXfDdkEWylgoNnZ+4MG1lNFqa8aO7F62tX0Yj5khjC0Bs7Mb2cHLx1XZaxJV6qSaulDuBbLYe8QUZXkMc7wmob3PM0kflfolR3LE7LResIHWa4j4FL6r5cQmFlDU2BDPpKMFMGUfRSFiUtaWBNXFOWHQBC2+uKmuMPYP4vJC9sBgqMvPN/X2KyemqdMvdKXnCfrzadHuSSJYEzD64Cve5Zl9yVvY4AqyBD aws-key
```


Der Root-Benutzer ist nicht deaktiviert und kann sich weiterhin anmelden. Dies ist nützlich, um Administrationsaufgaben durchzuführen:

```
disable_root: false
```


Aktiviert die automatische Aktualisierung der Paketliste, bevor weitere Pakete installiert werden. Dies stellt sicher, dass die neuesten Versionen der Software verwendet werden:

```
package_update: true
```


Beginnt den Block für die Liste der Pakete, die bei der Bereitstellung der Instanz installiert werden sollen:

```
packages:
```

Fügt das Paket curl zur Installationsliste hinzu. curl ist ein Tool zur Über:

```
  - curl
```




