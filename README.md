CyVerse Ansible check ssh connection
===================

This role checks for a connection and sets ansible_user to whatever was able to connect.

Requirements
------------

This role is only made to check Ubuntu CentOS and Rocky.

Role Variables
--------------

The following table lists optional ansible variables along with the default values if not defined.

Variable Name | Default value if not defined | Description
------------- | ---------------------- | -----------
SSH_TIMEOUT      | 30 | The time given to connect to the machine in seconds.
SSH_OPTIONS      | None | any additional options used for the ssh connection.
ansible_port     | 22 | The port used to connect to the machine.

Example Playbook
----------------

This is a sample playbook:
````
- hosts: host
  roles:
    - ansible_check_ssh_connection
  vars:
    SSH_TIMEOUT: 60
````

Author Information
------------------
Ryan Schneider (rschneider@cyverse.org)
