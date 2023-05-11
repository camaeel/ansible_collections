Install packages
=========

Install system packages for Ubuntu and Debian systems family.


Role Variables
--------------

add_packages_list - list of package names to isntall
remove_packages_list - list of package names to remove from system
sources_keys - list of apt keys to add (for custom apt repositories)
sources_repos - list of source repos entries (for custom apt repositories)
unattended_upgrades_all - Configure unattended upgrades

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
      - role: camaeel.install_packages
        add_packages_list:
        - vim
        remove_packages_list:
        - snapd
        sources_keys:
        - AJDSGFJSGDFJ765654
        sources_repos:
        - deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable     
        remove_sources_repos:
        - deb [arch=amd64] https://download.docker.com/linux/ubuntu DEPRECATED stable    
        unattended_upgrades_all: True

License
-------

Apache 2.0

