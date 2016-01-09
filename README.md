# Ansible Role: Install ansible from source

[![Build Status](https://travis-ci.org/tschifftner/ansible-role-ansible-source.svg)](https://travis-ci.org/tschifftner/ansible-role-ansible-source)

Installs ansible from source on Debian/Ubuntu linux servers. This allows to use ansible 2.0.0+

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

```
ansible_source_version: '2.0.0'
ansible_source_download_url: 'https://github.com/ansible/ansible/archive/v2.0.0-0.9.rc4.zip'
```

## Dependencies

None.

## Installation

```
$ ansible-galaxy install tschifftner.ansible-source
```

## Example Playbook

    - hosts: server
      roles:
        - { role: tschifftner.ansible-source }

## License

MIT / BSD

## Author Information

 - Tobias Schifftner, @tschifftner