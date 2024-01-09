Ansible Role: Qlik Sense site configuration
=========

An Ansible role that configures site settings for Qlik Sense Enterprise.

Requirements
------------

None.

Role Variables
--------------

```yaml
site_hostname: sense-cn.domain.tld
site_license_key: AAAnfwebnfl...
site_license_name: Your Name
site_license_org: Your Company
```

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
- hosts: central_node
  roles:
    - role: qlik.sense.site
      site_license_key: "{{ qlik_sense_slk }}"
      site_license_name: Adam Haydon
      site_license_org: Qlik
```

License
-------

MIT

Author Information
------------------

This role was created by [Adam Haydon](https://github.com/ahaydon) of [Qlik Customer Success](https://github.com/QlikProfessionalServices)
