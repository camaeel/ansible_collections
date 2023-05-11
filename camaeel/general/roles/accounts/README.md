Install packages
=========

Features:
- Create user accounts, 
- upload their ssh keys
- setup sudoers
- sshd tweaks
  - disable root login
  - disable password login


Role Variables
--------------

linux_users - list of users with groups and ssh keys
sudoers_all_enabled - enables creation of sudoers default rule, default: true
sshd_hardening - enables sshd security tweaks, default: true

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
      - role: camaeel.general.accounts
        users:
        - name: kamil
          groups: sudo
          keys:
          - ssh-rsa KEY1 CONTENTS
          - ssh-rsa KEY2 CONTENTS
        - name: john
          groups: ""
          keys: []

License
-------

Apache 2.0

