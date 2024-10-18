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

ssh_pwauth: false
disable_root: false
package_update: true
package_upgrade: true

packages:
  - apache2
  - php
  - libapache2-mod-php
  - php-mysqli
  - adminer

runcmd:
  - sudo systemctl enable apache2
  - sudo a2enconf adminer
  - sudo systemctl reload apache2
  - sudo systemctl status apache2 >> /home/ubuntu/apache_logs.log

write_files:
  - path: /var/www/html/index.html
    content: |
      <!DOCTYPE html>
      <html>
      <body>
      <h1>Hello world!</h1>
      <p>This is a text.</p>
      </body>
      </html>

  - path: /var/www/html/info.php
    content: |
      <?php
      // M346: Zeige alle Informationen, defaults to INFO_ALL
      phpinfo();
      ?>

  - path: /var/www/html/db.php
    content: |
      <?php
      // M346 database
      $servername = "172.31.41.82"; // Private IP des Datenbankservers
      $username = "admin"; // Benutzername
      $password = "12Luka21"; // Passwort
      $dbname = "mysql";

      // Create connection
      $conn = new mysqli($servername, $username, $password, $dbname);
      // Check connection
      if ($conn->connect_error) {
          die("Connection failed: " . $conn->connect_error);
      }

      $sql = "SELECT Host, User FROM mysql.user;";
      $result = $conn->query($sql);
      while($row = $result->fetch_assoc()) {
          echo($row["Host"] . " / " . $row["User"] . "<br />");
      }
      ?>
