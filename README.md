Generic hostname setup ansible role
==============================

This Ansible role setup hostname of target hosts according to `inventory_hostname` (from inventory file) and `parent_dns_zone` (from `defaults/main.yml`) Ansible variables.cd 

It's also can add to `/etc/host` file on targeted host(s) all your hosts with IP (based on `ansible_ssh_host` variable) from inventory file. This optional task will do if you will set `all_hostnames_deploy` variable to `yes` while run the playbook.

Requirements
------------

See [meta/main.yml](meta/main.yml)

Role Variables
--------------

See [defaults/main.yml](defaults/main.yml)

Dependencies
------------

See [meta/main.yml](meta/main.yml)

Example Playbook
----------------

```yml
- hosts: all
  roles:
    - generic.hostname-to-inventoryname-setup
```

License
-------

MIT

Author Information
------------------

Andrey Makarov <mb@mcrrw.me>
