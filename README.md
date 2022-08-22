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

## Role Information

See the individual roles for variable descriptions.

- [ansible-role-configure_firewall](https://github.com/glillico/ansible-role-configure_firewall)<br>
- [ansible-role-set_hostname](https://github.com/glillico/ansible-role-set_hostname)<br>
- [ansible-role-update_pkgs](https://github.com/glillico/ansible-role-update_pkgs)<br>
- [ansible-role-reboot_server](https://github.com/glillico/ansible-role-reboot_server)<br>
- [ansible-role-configure_ntp](https://github.com/glillico/ansible-role-configure_ntp)<br>
- [ansible-role-configure_sshd](https://github.com/glillico/ansible-role-configure_sshd)<br>
- [ansible-role-install_fail2ban](https://github.com/glillico/ansible-role-install_fail2ban)<br>
- [ansible-role-auto_pkg_updates](https://github.com/glillico/ansible-role-auto_pkg_updates)<br>
- [ansible-role-setup_users](https://github.com/glillico/ansible-role-setup_users)<br>
- [ansible-role-configure_sudo](https://github.com/glillico/ansible-role-configure_sudo)<br>
- [ansible-role-setup_ssh_keys](https://github.com/glillico/ansible-role-setup_ssh_keys)<br>
- [ansible-role-copy_etc_issue](https://github.com/glillico/ansible-role-copy_etc_issue)

## License

MIT

## Author Information

Created in 2022 by Graham Lillico.
