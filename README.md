Apt
===

Configure apt-get for ubuntu

Role Variables
--------------

Variables that are available for configuration are:

    - `periodic_updates`: Enable/disable periodic updates, default: true
    - `force_ipv4`: Force ipv4 ony, default: true
    - `unattended_upgrades`: Enable/disable unattended security updates, default: true
    - `unattended_upgrades_email`: Unattended upgrades failure notification email, default 'root@localhost'

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    ---
    - hosts: all
      roles:
        - apt

License
-------

BSD
