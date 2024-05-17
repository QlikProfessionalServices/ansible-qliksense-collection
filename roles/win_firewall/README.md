Ansible Role: Windows Firewall rules for Qlik Sense
=========

An Ansible role that creates Windows Firewall rules for Qlik Sense Enterprise.

Requirements
------------

None.

Role Variables
--------------

```yaml
win_firewall_db_port: 4432
```

Dependencies
------------

None.

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
    - role: qlik.sense.win_firewall
      win_firewall_db_port: 5432
```

License
-------

MIT

Author Information
------------------

This role was created by [Adam Haydon](https://github.com/ahaydon) of [Qlik Customer Success](https://github.com/QlikProfessionalServices)
