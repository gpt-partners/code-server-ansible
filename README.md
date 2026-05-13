# Code Server

Execute

```
ansible-playbook -i inventory.ini install-code-server.yml -e "ansible_host=server_ip"
```

# Caddy

Execute

```
ansible-playbook -i inventory.ini install-caddy.yml -e "ansible_host=server_ip" -e "domain_name=dname"
```


# Kasm

## Prerequisites

Set your server IP and admin password in `inventory.ini`:

```ini
kasm_server ansible_host=YOUR_SERVER_IP ansible_user=root

[kasm_server:vars]
admin_password=CHANGE_ME
```

> **Required:** `admin_password` must be set before running. The admin login is `admin@kasm.local`.

## Execute

```
ansible-playbook -i inventory.ini install-kasm.yml -e "ansible_host=server_ip" -e "admin_password=yourpassword"
```

After install, access Kasm at `https://server_ip:8443`.
