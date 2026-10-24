# ansible-role-apache24

[![Build Status](https://github.com/systemli/ansible-role-apache24/workflows/Integration/badge.svg?branch=main)](https://github.com/systemli/ansible-role-apache24/actions?query=workflow%3AIntegration)
[![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-apache24-blue.svg)](https://galaxy.ansible.com/systemli/apache24/)

Install and configure Apache 2.4

## Role Variables

see `defaults/main.yml`. The accepted variables and their types are also declared in `meta/argument_specs.yml`.

## Download

Download latest release with `ansible-galaxy`

$ ansible-galaxy install systemli.apache24

## Example Playbook

```
- hosts: servers
  roles:
    - { role: systemli.apache24 }
```

## Testing & Development

The role is tested with GitHub Actions, using Molecule with the Docker driver on Debian 12 (bookworm) and Debian 13 (trixie). Locally you need Docker, `molecule`, `molecule-plugins[docker]` and `ansible-lint`.

```
molecule test       # full test run
molecule converge   # apply the role to a container
molecule login      # open a shell in the container
ansible-lint .      # lint the role
```

## License

GPL

## Author Information

https://www.systemli.org
