Ansible Role: Qlik Sense Application Management Console
=========

An Ansible role to deploy the Application Management Console for Qlik Sense.

Requirements
------------

None.

Role Variables
--------------

```yaml
amc_library_name: AMC
amc_base_uri: https://{{ ansible_facts.hostname }}
```

Dependencies
------------

None.

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
      - role: qlik.sense.amc
```

License
-------

MIT

Author Information
------------------

This role was created by [Adam Haydon](https://github.com/ahaydon) of [Qlik Customer Success](https://github.com/QlikProfessionalServices).
