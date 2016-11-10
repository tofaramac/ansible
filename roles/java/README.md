java
====

[![Ansible Role](https://img.shields.io/ansible/role/3309.svg)](https://galaxy.ansible.com/list#/roles/3309)

Installs Java

Requirements
------------

This role requires Ansible 1.4 or higher.

Role Variables
--------------

| Name                           | Default | Description                                           |
|--------------------------------|---------|-------------------------------------------------------|
| java_implementation            | openjdk | Java implementation to install, openjdk or oracle     |
| java_openjdk_version           | 8       | Version of OpenJDK Java to install                    |
| java_openjdk_headless          | false   | Select 'Complete' vs 'Headless' install for OpenJDK   |
| java_openjdk_jre_only          | false   | Select JDK vs Java Runtime Environment for OpenJDK    |
| java_openjdk_use_ppa           | true    | Add the OpenJDK-R Java PPA to repositories list       |
| java_oracle_version            | 8       | Version of Oracle Java to install                     |
| java_oracle_install_jce_policy | false   | Enable/Disable installation of Oracle Java JCE policy |

Dependencies
------------

None

Example Playbook
----------------

Install OpenJDK Java 8
```
- hosts: all
  roles:
    - { role: kbrebanov.java }
```

Install OpenJDK Java 7 (headless, JRE-only)
```
- hosts: all
  roles:
    - { role: kbrebanov.java, java_openjdk_version: 7, java_headless: true, java_jre_only: true }
```

Install Oracle Java 8
```
- hosts: all
  roles:
    - { role: kbrebanov.java, java_implementation: oracle }
```

Install Oracle Java 8 and JCE policy
```
- hosts: all
  roles:
    - { role: kbrebanov.java, java_implementation: oracle, java_oracle_install_jce_policy: true }
```

Install Oracle Java 7
```
- hosts: all
  roles:
    - { role: kbrebanov.java, java_implementation: oracle, java_oracle_version: 7 }
```

Install Oracle Java 7 and JCE policy
```
- hosts: all
  roles:
    - { role: kbrebanov.java, java_implementation: oracle, java_oracle_version: 7, java_oracle_install_jce_policy: true }
```

License
-------

BSD

Author Information
------------------

Kevin Brebanov
