# Ansible Role: Sysctl

[![Build Status](https://travis-ci.org/AttestationLegale/ansible-role-sysctl.svg?branch=master)](https://travis-ci.org/AttestationLegale/ansible-role-sysctl) [![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-sysctl-blue.svg)](https://galaxy.ansible.com/list#/roles/5400)

Manage `sysctl` settings.

## Requirements

None

## Role Variables

* `sysctl_settings`: [default: `[]`]: List of `sysctl` settings
* `sysctl_settings.{n}.name`: [required]: Name of the setting
* `sysctl_settings.{n}.value`: [required]: Value of the setting
* `sysctl_settings.{n}.state`: [default: `present`]: Whether to ensure the setting is present or absent

## Dependencies

None

## Example Playbook

```yaml
---
- hosts: all
  roles:
    - sysctl
  vars:
    sysctl_settings:
      - name: net.ipv4.tcp_fin_timeout
        value: 10
```

## License

MIT / BSD

## Author Information

This role was created in 2016 by [ALG](https://www.attestationlegale.fr), based on a fork of [ansible-sysctl](https://github.com/Oefenweb/ansible-sysctl).
