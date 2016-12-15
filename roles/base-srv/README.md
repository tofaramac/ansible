Ubuntu Server Provisioning
========

Upgrades existing Basic Ubuntu Server packages and utility packages required

Requirements
------------

Ubuntu Server
OpenSSH Port 201
ssh key public

Role Variables
--------------

none

Dependencies
------------

none

Example Playbook
-------------------------

ansible-playbook server-ubuntu.yml --ask-sudo-pass --extra-vars "target=sean-test"

Author Information
------------------

Sean Wheller
