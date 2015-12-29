# Ansible Role: Install ansible from source

[![Build Status](https://travis-ci.org/tschifftner/ansible-role-ansible-source.svg)](https://travis-ci.org/tschifftner/ansible-role-ansible-source)

Installs ansible from source on Debian/Ubuntu linux servers. This allows to use ansible 2.0.0+

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

```
ansible_git_version: "stable-2.0" # This can be the full 40-character SHA-1 hash, the literal string HEAD, a branch name, or a tag name.
ansible_repo_url: "https://github.com/ansible/ansible.git"
ansible_install_dir: "/opt/ansible"
ansible_required_packages:
  - "python-pip"
  - "python-dev"
  - "git"

ansible_pip_install:
  - "PyYAML"
  - "jinja2"
  - "paramiko"
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