# ansible-role-apache24

[![Build Status](https://github.com/systemli/ansible-role-apache24/workflows/Integration/badge.svg?branch=main)](https://github.com/systemli/ansible-role-apache24/actions?query=workflow%3AIntegration)
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

For developing and testing the role we use Github Actions, Molecule, and Docker. On the local environment you can easily test the role with

Run local tests with:

```
molecule test
```

Requires Molecule and Docker.

## License

GPL

## Author Information

https://www.systemli.org
