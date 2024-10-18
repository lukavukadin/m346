````

#cloud-config
users:
  - name: ubuntu
    sudo: ALL=(ALL) NOPASSWD:ALL
    groups: users, admin
    home: /home/ubuntu
    shell: /bin/bash
    ssh-authorized-keys:
      - ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDhQ8vwJIRsyfGmiAMOVHa5zewH0QzAcgDTmuy5Xi+VL93iJzep7PaalZ9eWLqiMn+r2XQ6yddldnwhl6fswq6vpgDw4QZFvuT0azGwcOF0LMWzikuIj9G/spAutVubwFyivY46msuloGVn3fFY+Q6YsiIQCvLLrJQFE1ZAvF+lqGgW6V24Wo40WpEU+0m2EaU4VSbqmGegHSkEGl7lT4orwzQ/BgFmAFB+yyyzPQkYl1OVSO1JHAkWdj5g+ESWg8K7p9OgIut608C8KybwaSxCLQy9D4dFZVZJBROx172LvPcUVJ5n1cZ1B9ZfKx42YHo52wJCX6RLJd1DwUbY51eF lukas

ssh_pwauth: false
disable_root: false
package_update: true
packages:
  - curl
  - wget
