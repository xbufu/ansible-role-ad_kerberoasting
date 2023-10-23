Ansible Role: AD Kerberoasting.
=========

An Ansible role to enable Kerberoasting attack on a number of users in the domain.

Requirements
------------

Needs to be run on the DC.

Role Variables
--------------

```yml
num_kerberoastable_users: 1
spn_services:
  - https
  - ftp
  - CIFS
  - kafka
  - MSSQL
  - POP3
spn_action: add
```

Dependencies
------------

None.

Example Playbook
----------------

```yml
- hosts: pdc01
  roles:
    - role: xbufu.ad_kerberoasting
      vars:
        num_kerberoastable_users: 1
        spn_services:
          - https
          - ftp
          - CIFS
          - kafka
          - MSSQL
          - POP3
        spn_action: add
```

License
-------

MIT / BSD

Author Information
------------------

Created by xbufu.
