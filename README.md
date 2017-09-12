# ansible-gitconfig

Ansible role to configure git.

[![Build Status](https://img.shields.io/travis/feffi/ansible-gitconfig.svg)](https://github.com/feffi/ansible-gitconfig) [![Github All Releases](https://img.shields.io/github/downloads/feffi/ansible-gitconfig/total.svg)](https://github.com/feffi/ansible-gitconfig) [![GitHub forks](https://img.shields.io/github/forks/feffi/ansible-gitconfig.svg?style=social&label=Fork)](https://github.com/feffi/ansible-gitconfig) [![GitHub stars](https://img.shields.io/github/stars/feffi/ansible-gitconfig.svg?style=social&label=Star)](https://github.com/feffi/ansible-gitconfig) [![GitHub watchers](https://img.shields.io/github/watchers/feffi/ansible-gitconfig.svg?style=social&label=Watch)](https://github.com/feffi/ansible-gitconfig) [![Twitter Follow](https://img.shields.io/twitter/follow/feffi1.svg?style=social&label=Follow)](https://twitter.com/feffi1) [![License](http://img.shields.io/:license-mit-blue.svg)](https://github.com/feffi/ansible-gitconfig/blob/master/LICENSE)

## Role Defaults Variables

```yaml
# Sections and key-value pairs to include in the users .gitconfig
gitconfig:
  config:
    <section>:
      <key>: <value>
      <key>: <value>
      ...

  # Lines to be included in users global .gitignore file
  ignores:
    - ".vagrant"
    - ".DS_Store"
```

Example:

```yaml
- hosts: all
  vars:
    gitconfig:
      config:
        user:
          name: Your Name
          email: your-email@exemple.org
      ignores:
        - ".vagrant"
        - ".DS_Store"

  roles:
    - { role: feffi.gitconfig }
```
