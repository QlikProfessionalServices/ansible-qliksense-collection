Ansible Role: Qlik Sense Node
=========

An Ansible role to configure Qlik Sense node settings.

Requirements
------------

None.

Role Variables
--------------

```yaml
node_central_inventory: sense-cn
node_central_hostname: sense-cn
node_name: Engine Node
node_hostname: sense-rim1
node_purpose: Production
node_failover_candidate: false
node_engine_enabled: "{{ node_failover_candidate }}"
node_proxy_enabled: "{{ node_failover_candidate }}"
node_scheduler_enabled: "{{ node_failover_candidate }}"
node_printing_enabled: "{{ node_failover_candidate }}"
```

Dependencies
------------

None.

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
    - role: qlik.sense.node
      node_name: "{{ inventory_hostname }}"
      node_hostname: "{{ inventory_hostname }}"
      node_purpose: ProductionAndDevelopment
      node_engine_enabled: yes
      node_printing_enabled: yes
      node_central_inventory: "{{ groups['central_nodes'] | first }}"
```

License
-------

MIT

Author Information
------------------

This role was created by [Adam Haydon](https://github.com/ahaydon) of [Qlik Customer Success](https://github.com/QlikProfessionalServices)
