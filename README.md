A role to install AIDE (Advanced Intrusion Detection Environment) via Ansible
=========

Role Variables
--------------

```
aide_new_db - Used by the handler in handlers/main.yml to determine where to put the new aide database
aide_db -  Used by the handler in handlers/main.yml to know where the current aide database is
aide_email_to - In /etc/default/aide where the email reports are to be sent.
aide_quiet_reports - In /etc/default/aide set to yes if you don't want reports when nothing has changed
aide_ignore_list - In /etc/aide/aide.conf this is a list of all the things your adding to the excludes list
aide_checksums - In /etc/ainde/aide.conf you can choose how many checksums to run. If you want to sacrifice security for speed, just use 1.

```

In your vars you'll want to define a list of things/paths/files to ignore for the aide_ignore_list var like so:
```
    - { regex: 'what to match ', line: 'replace with this ' }
For example:
    - { regex: '^!/some/path', line: '!/some/path/.*' }
```

Example Playbook
----------------

```ansible-playbook -i [inventory] -u [user] -K ./aide.yml --limit=[server] --tags=install```

Author Information
------------------

Blake Carver
