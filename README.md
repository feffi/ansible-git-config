# ansible-git-config
Ansible role to configure the global gitconfig and .gitignore.

[![Build Status](https://img.shields.io/travis/feffi/ansible-git-config.svg)](https://travis-ci.org/feffi/ansible-git-config) [![Github All Releases](https://img.shields.io/github/downloads/feffi/ansible-git-config/total.svg)](https://github.com/feffi/ansible-git-config) [![GitHub forks](https://img.shields.io/github/forks/feffi/ansible-git-config.svg?style=social&label=Fork)](https://github.com/feffi/ansible-git-config) [![GitHub stars](https://img.shields.io/github/stars/feffi/ansible-git-config.svg?style=social&label=Star)](https://github.com/feffi/ansible-git-config) [![GitHub watchers](https://img.shields.io/github/watchers/feffi/ansible-git-config.svg?style=social&label=Watch)](https://github.com/feffi/ansible-git-config) [![Twitter Follow](https://img.shields.io/twitter/follow/feffi1.svg?style=social&label=Follow)](https://twitter.com/feffi1) [![License](http://img.shields.io/:license-mit-blue.svg)](https://github.com/feffi/ansible-git-config/blob/master/LICENSE)

## Role Defaults Variables

```yaml
# Sections and key-value pairs to include in the users .git-config
ansible_git_config: {
  dest: "/home/feffi/.gitconfig",
  config: {
    <section>: {
      <key>: <value>,
      <key>: <value>,
      ...
    }
  },
  # Lines to be included in users global .gitignore file
  ignores: [
    ".vagrant"
    ".DS_Store"
  ]
```

Example:

```yaml
- hosts: all
  vars:
    ansible_git_config:
      dest: "/home/feffi/.gitconfig"
      config:
        user:
          name: Your Name
          email: your-email@example.org
      ignores:
        - ".vagrant"
        - ".DS_Store"
  roles:
    - { role: ansible-git-config }
```
