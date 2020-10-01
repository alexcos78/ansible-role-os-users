OS Users
========

This role is used for users management.

Role Variables
--------------

The role accept a list with the following items:

``os_user_name``: set user name.
``os_user_guid``: set user GUID, if you do not want to set a specific GUID for the user omit it, it will be randomly assinged.
``os_user_ssh_public_key``: SSH public key of the user.


Example Playbook
----------------

```
---
- name: role for adding users
  hosts: server
  vars:
    os_users: 
      - { os_user_name: "username", os_user_guid: "<uid>", os_user_ssh_public_key: "ssh-key.pub"}
      - { os_user_name: "username", os_user_ssh_public_key: "ssh-key.pub" }
  roles:
    - role: indigo-dc.os-users

```

License
-------
Apache Licence v2

