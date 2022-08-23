# server-setup

An ansible playbook that runs a number of roles that together perform some basic server setup and hardening.

## Usage

- Clone this repository.
    - `$ git clone https://github.com/glillico/server-setup.git`
  - Change to the repositories directory.
    - `$ cd server-setup`
  - Install requirements.
    - `$ ansible-galaxy install -r requirements.yml`
  - Make a copy of the file `example.config.yml` and modify it to meet your requirements.
    - `$ cp example-config.yml config.yml`
  - Make a copy of the file `example.inventory.ini` and modify it to meet your requirements.
    - `$ cp example-inventory.ini inventory.ini`
  - Copy the ssh keys for your initial user into the `keys` directory, and modify the `config.yml` file appropriately. 
  - Run the playbook.
    - `$ ansible-playbook main.yml`

## Using tags

- It is possible run a specifc section of the playbook by using the `ansible-playbook`'s `--tags` feature.
    - `$ ansible-playbook main.yml -t "docker,reboot"`
- The available tage are 
    - `auto_pkg_updates`, `docker`, `fail2ban`, `firewall`, `hostname`, `issue`, `ntp`, `reboot`, `ssh_keys`, `sshd`, `sudo`, `update_pkgs`, `users`

## Role Information

See the individual roles for variable descriptions.

- [ansible-role-auto_pkg_updates](https://github.com/glillico/ansible-role-auto_pkg_updates)<br>
- [ansible-role-configure_firewall](https://github.com/glillico/ansible-role-configure_firewall)<br>
- [ansible-role-configure_ntp](https://github.com/glillico/ansible-role-configure_ntp)<br>
- [ansible-role-configure_sshd](https://github.com/glillico/ansible-role-configure_sshd)<br>
- [ansible-role-configure_sudo](https://github.com/glillico/ansible-role-configure_sudo)<br>
- [ansible-role-copy_etc_issue](https://github.com/glillico/ansible-role-copy_etc_issue)
- [ansible-role-install_docker](https://github.com/glillico/ansible-role-install_docker)<br>
- [ansible-role-install_fail2ban](https://github.com/glillico/ansible-role-install_fail2ban)<br>
- [ansible-role-reboot_server](https://github.com/glillico/ansible-role-reboot_server)<br>
- [ansible-role-set_hostname](https://github.com/glillico/ansible-role-set_hostname)<br>
- [ansible-role-setup_ssh_keys](https://github.com/glillico/ansible-role-setup_ssh_keys)<br>
- [ansible-role-setup_users](https://github.com/glillico/ansible-role-setup_users)<br>
- [ansible-role-update_pkgs](https://github.com/glillico/ansible-role-update_pkgs)<br>

## License

MIT

## Author Information

Created in 2022 by Graham Lillico.
