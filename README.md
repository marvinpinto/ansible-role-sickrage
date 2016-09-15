sickrage
========

[![Build Status](https://img.shields.io/travis/marvinpinto/ansible-role-sickrage/master.svg?style=flat-square)](https://travis-ci.org/marvinpinto/ansible-role-sickrage)
[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-sickrage-blue.svg?style=flat-square)](https://galaxy.ansible.com/marvinpinto/sickrage)
[![License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE.txt)

Ansible Galaxy role to install and manage [sickrage](https://sickrage.github.io).


Requirements
------------

This role has been tested on Ubuntu 14.04 and will likely only work on an
Ubuntu-like system.


Role Variables
--------------

``` yaml
# Application config
sickrage_app_src_directory: '/opt/sickrage_src'
sickrage_app_data_directory: '/opt/sickrage_data'
sickrage_app_pid_file: '/tmp/sickrage.pid'

# Daemon config
sickrage_daemon_user: 'sickdaemon'
sickrage_daemon_port: '8081'
sickrage_daemon_extra_opts: " --port={{ sickrage_daemon_port }}"
```


Examples
--------

Install this module from Ansible Galaxy into the './roles' directory:
```bash
ansible-galaxy install marvinpinto.sickrage -p ./roles
```

Use it in a playbook as follows:
```yaml
- hosts: '127.0.0.1'
  roles:
    - role: 'marvinpinto.sickrage'
      become: true
```


Development
-----------
Use the supplied `Vagrantfile` for local development and testing (hint: `vagrant up --provision`)
