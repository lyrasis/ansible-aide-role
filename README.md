A role to install AIDE (Advanced Intrusion Detection Environment) via Ansible
=========


DON'T USE THIS YET IT'S WAY BROKEN
=========

I'll have it cleaned up soon :-)

Role Variables
--------------

```
email_to - In etc/aide where the email reports are to be sent.
checksums - In aide.conf you can choose how many checksums to run. If you want to sacrifice security for speed, just use 1.
aide_new_db - Used by the handler to determine where to put the new aide database
aide_db -  Used by the handler to know where the current aide database is
quiet_reports - set to yes if you don't want reports when nothing has changed
```

Example Playbook
----------------

```ansible-playbook -i [inventory] -u [user] -K ./aide.yml --limit=[server] --tags=install```

Author Information
------------------

Blake Carver
