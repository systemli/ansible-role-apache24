# ansible-role-apache24

[![Build Status](https://travis-ci.com/systemli/ansible-role-apache24.svg?branch=master)](https://travis-ci.com/systemli/ansible-role-apache24)
[![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-apache24-blue.svg)](https://galaxy.ansible.com/systemli/apache24/)

Install and configure Apache 2.4

## Role Variables

see `defaults/main.yml`

## Download

Download latest release with `ansible-galaxy`

$ ansible-galaxy install systemli.apache24

## Example Playbook

```
- hosts: servers
  roles:
    - { role: systemli.apache24 }
```

Testing & Development
---------------------

Tests
-----

For developing and testing the role we use Travis CI, Molecule and Vagrant. 

Run local tests with:

```
molecule test 
```

This requires Molecule, Vagrant and `python-vagrant` to be installed.

## License

GPL

## Author Information

https://www.systemli.org
