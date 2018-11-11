# ansible-pacman

Ansible role to configure/add a pacman.

[![Build Status](https://img.shields.io/travis/feffi/ansible-pacman.svg)](https://travis-ci.org/feffi/ansible-pacman) [![Github All Releases](https://img.shields.io/github/downloads/feffi/ansible-pacman/total.svg)](https://github.com/feffi/ansible-pacman) [![GitHub forks](https://img.shields.io/github/forks/feffi/ansible-pacman.svg?style=social&label=Fork)](https://github.com/feffi/ansible-pacman) [![GitHub stars](https://img.shields.io/github/stars/feffi/ansible-pacman.svg?style=social&label=Star)](https://github.com/feffi/ansible-pacman) [![GitHub watchers](https://img.shields.io/github/watchers/feffi/ansible-pacman.svg?style=social&label=Watch)](https://github.com/feffi/ansible-pacman) [![Twitter Follow](https://img.shields.io/twitter/follow/feffi1.svg?style=social&label=Follow)](https://twitter.com/feffi1) [![License](http://img.shields.io/:license-mit-blue.svg)](https://github.com/feffi/ansible-pacman/blob/master/LICENSE)
## Requirements

- Ansible 2.7.1
- pacman ;-)

### ansible.cfg

```yaml
hash_behaviour = merge
```

## Install

Just add the role to your ``requirements.yml`` file:

```yaml
- src: https://github.com/feffi/ansible-pacman.git
  name: ansible-pacman
```

## Role Defaults Variables

```yaml
ansible_pacman: {
  # The mirror country to use
  mirror: "DE",
  # Packages to install
  install: [],
  # Packages to remove
  remove: []
}
```

Example:

```yaml
- hosts: all
  vars:
    ansible_pacman:
      # The mirror country to use
      mirror: "DE"
      # Packages to install
      install: []
      # Packages to remove
      remove: []
  roles:
    - { role: ansible-pacman }
```
