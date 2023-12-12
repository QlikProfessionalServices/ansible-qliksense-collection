Ansible Role: Qlik Sense download
=========

An Ansible Role that downloads Qlik Sense setup and updates from GitHub.

Requirements
------------

None.

Role Variables
--------------

```yaml
release_name: November 2023 Initial Release
patch_name: November 2023 Patch 1
download_path: "{{ lookup('ansible.builtin.env', 'HOME') }}/Downloads"
setup_path: "{{ download_path }}/{{ release_name }}/Qlik_Sense_setup.exe"
patch_path: "{{ download_path }}/{{ patch_name }}/Qlik_Sense_update.exe"
```

Dependencies
------------

None.

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
    - role: qlik.sense.download
      release_name: November 2023 Initial Release
      patch_name: November 2023 Patch 1
```

License
-------

MIT

Author Information
------------------

This role was created by [Adam Haydon](https://github.com/ahaydon) of [Qlik Customer Success](https://github.com/QlikProfessionalServices)
