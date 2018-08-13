Custom Prometheus-monitoring custom targets Ansible role
==============================

This Ansible role create target file for 
[Prometheus custom service discovery](https://prometheus.io/blog/2015/06/01/advanced-service-discovery/#custom-service-discovery)
and add to this file all hosts from Ansible inventory.

**Note:** you need to (re)define `prometheus_custom_targets_path` variable
before run thois role and configure your Prometheus server to use this cusdtom
path (according to [article](https://prometheus.io/blog/2015/06/01/advanced-service-discovery/#custom-service-discovery)).

**Original repo:** https://github.com/anmcarrow/anmcarrow.ansible.prometheus-targets-from-inventory-setup 

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
    - generic.prometheus-targets-from-inventory-setup
```

License
-------

MIT

Author Information
------------------

Andrey Makarov <mb@mcrrw.me>
