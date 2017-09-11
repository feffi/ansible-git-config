# ansible-gitconfig

Ansible role to configure git.

[![Build Status](https://travis-ci.org/feffi/ansible-gitconfig.svg?branch=master)](https://travis-ci.org/feffi/ansible-gitconfig)

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
