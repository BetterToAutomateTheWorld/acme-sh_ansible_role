verosk.acme-sh
==============

This role sets-up [acme.sh][acme] on the target host. The role does not generate any certificates (yet).

It's started as proof of concept but I've found myself to use it for more
than two years.

Originally written by VerosK and modified by Darcidride.

Changelog for the Darcidride tweaks
--------------

- Don't use "sudo" rights on all tasks but only on specific tasks
- Fix some rights issue because don't use anymore "sudo" on all tasks
- Fix some issues about acme certificates generation on Ubuntu 14.04
- Fix some issues about Nginx reload/restart on Ubuntu 14.04
- Fix compatibility issues between ansible 2.1.0 and 2.4.0 execution
- Some rights tweaks
- Typo fix on task comments

This script was originally made to be executed with Ansible 2.1.0, now it can be executed with Ansible 2.4.0


Role Variables
--------------

Please check `defaults/main.yml`

Dependencies
------------

This role has no dependencies.  But `nc` should be probably installed on
the target host to start `acme.sh`.

Example Playbook
----------------

    - hosts: webservers
      roles:
         - role: VerosK.acme-sh

License
-------

BSD-2 || WTFPL

Author Information
------------------

This role was prepared by Věroš Kaplan,
sponsored by [vpsfree.cz][vpsfree]

[vpsfree]: https://vpsfree.cz
[acme]: https://github.com/Neilpang/acme.sh
