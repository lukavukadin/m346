````
#cloud-config
users:
  - name: ubuntu
    sudo: ALL=(ALL) NOPASSWD:ALL
    groups: users, admin
    home: /home/ubuntu
    shell: /bin/bash
    ssh-authorized-keys:
      - ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDhQ8vwJIRsyfGmiAMOVHa5zewH0QzAcgDTmuy5Xi+VL93iJzep7PaalZ9eWLqiMn+r2XQ6yddldnwhl6fswq6vpgDw4QZFvuT0azGwcOF0LMWzikuIj9G/spAutVubwFyivY46msuloGVn3fFY+Q6YsiIQCvLLrJQFE1ZAvF+lqGgW6V24Wo40WpEU+0m2EaU4VSbqmGegHSkEGl7lT4orwzQ/BgFmAFB+yyyzPQkYl1OVSO1JHAkWdj5g+ESWg8K7p9OgIut608C8KybwaSxCLQy9D4dFZVZJBROx172LvPcUVJ5n1cZ1B9ZfKx42YHo52wJCX6RLJd1DwUbY51eF

packages:
  - apache2           # Installiert den Apache Webserver
  - php               # Installiert PHP
  - php-mysql         # Installiert das PHP-MySQL Modul für die Verbindung zur Datenbank
  - adminer           # Installiert Adminer für die Datenbankverwaltung

write_files:
  - path: /var/www/html/index.html
    content: |
      <html><body><h1>Hello from Web Server</h1></body></html>  # Erstellen einer einfachen HTML-Seite
  - path: /var/www/html/info.php
    content: |
      <?php phpinfo(); ?>  # Erstellt eine PHP-Seite mit PHP-Info
  - path: /var/www/html/db.php
    content: |
      <?php
      $mysqli = new mysqli("DATABSE_IP", "admin", "PASSWORD", "DATABASE_NAME");
      if ($mysqli->connect_error) {
          die("Connection failed: " . $mysqli->connect_error);
      }
      echo "Connected successfully";
      ?>

runcmd:
  - sudo systemctl start apache2  # Startet den Apache-Dienst
  - sudo systemctl enable apache2   # Aktiviert Apache beim Systemstart
  - sudo a2enconf adminer           # Fügt Adminer zur Apache-Konfiguration hinzu
  - sudo systemctl restart apache2   # Startet den Apache-Dienst neu
