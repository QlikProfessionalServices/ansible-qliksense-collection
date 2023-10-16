Ansible Role: Qlik Sense setup
=========

An Ansible Role that installs Qlik Sense Enterprise on Windows.

Requirements
------------

None.

Role Variables
--------------

```yaml
setup_path: '{{ ansible_env.HOME }}\Downloads\Qlik_Sense_setup.exe'
accept_eula: yes
desktop_shortcut: no
skip_start_services: no
install_dir: D:\Apps\Qlik\Sense
user_with_domain: '{{ ansible_netbios_name }}\qservice'
user_password: "Qlik1234"
db_password: "Qlik1234"
hostname: sense-cn
shared_persistence_config: '{{ ansible_env.TEMP }}\spc.cfg'
send_data: no
skip_validation: no
database_dump_file: 'C:\backup\qsr.tar'
bundle_install:
  - dashboard
  - visualization

db_user_name: qliksenserepository
db_user_password: "Qlik1234"
db_host: localhost
db_port: 4432
root_dir: '\\{{ ansible_netbios_name }}\QlikShare'
apps_dir: '{{ root_dir }}\Apps'
static_content_root_dir: '{{ root_dir }}\StaticContent'
archived_logs_dir: '{{ root_dir }}\ArchivedLogs'
create_cluster: yes
install_local_db: yes
configure_db_listener: yes
listen_addresses:
  - 0.0.0.0
  - ::0
ip_range:
  - 0.0.0.0/0
  - ::0/0
max_connections: 100
http_port_number: 80
https_port_number: 443
enable_http_port: no
db_maximum_connection_pool_size: 1000
```

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
        - qlik.sense.setup
          setup_path: '{{ ansible_env.HOME }}\Downloads\Qlik_Sense_setup.exe'
          accept_eula: yes
          user_with_domain: '{{ ansible_netbios_name }}\qservice'
          user_password: "Qlik1234"
          db_user_password: "Qlik1234"
          db_password: "Qlik1234"
          root_dir: '\\{{ ansible_netbios_name }}\QlikShare'

License
-------

MIT

Author Information
------------------

This role was created by [Adam Haydon](https://github.com/ahaydon) of [Qlik Customer Success](https://github.com/QlikProfessionalServices)
