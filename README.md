OPNsense: Unbound DNS
=====================

An ansible role to manage the Unbound DNS server on an opnSense firewall.

Requirements
------------

This role requires the `lxml` python package to be installed on the host system.

Role Variables
--------------

|                Variable                 | Type  |                  Description                  |
| :-------------------------------------: | :---: | :-------------------------------------------: |
|        opnsense_unbound_enabled         | bool  |     Enable/Disable the unbound firewall.      |
|     opnsense_unbound_register_dhcp      | bool  |  Enable/Disable registration of dhcp leases.  |
| opnsense_unbound_register_static_leases | bool  | Enable/Disable registration of static leases. |
|     opnsense_unbound_dnssec_enabled     | bool  |            Enable/Disable dnssec.             |
|      opnsense_unbound_flush_cache       | bool  |          Enable/Disable cache flush.          |

Dependencies
------------

N/A.

Example Playbook
----------------

```yaml
- name: Configure the DNS
  hosts: opnsense

  roles:
    - role: mirceanton.opnsense_unbound
      vars:
        opnsense_unbound_enabled: true
        opnsense_unbound_register_dhcp: true
        opnsense_unbound_register_static_leases: true
        opnsense_unbound_dnssec_enabled: true
        opnsense_unbound_flush_cache: true
```

License
-------

MIT

Author Information
------------------

A role developed by [Mircea-Pavel ANTON](https://www.mirceanton.com).
