# Ansible HOWTO

## Install brew

Mac

```
brew install ansible
```

## Create an inventory file

```
echo "w.x.y.z" > inv.ini
```

## Test the connection

_This assumes you can SSH as root into the machine._

```
ansible all -i inv.ini -m ping -u root
```

## Run the playbook

```
ansible-playbook basic_security.yml -i inv.ini -u root
```

## Available playbooks

### `basic_security.yml`

- Unattended upgrades
- No SSH password authentication
- Custom SSH port (6677)
- Basic firewall configuration
- fail2ban
- logwatch notifying daily on dev@jobteaser.com


