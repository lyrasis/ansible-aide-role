A role to install AIDE (Advanced Intrusion Detection Environment) via Ansible
=========


DON'T USE THIS YET IT'S WAY BROKEN
=========

This installs AIDE, 

Requirements
------------

Installs all needed.

Role Variables
--------------

This needs the mail_to var changed to be a var

Dependencies
------------

Nothing

Example Playbook
----------------

```ansible-playbook -i [inventory] -u [user] -K ./aide.yml --limit=[server] --tags=install```


License
-------

BSD

Author Information
------------------

Blake
