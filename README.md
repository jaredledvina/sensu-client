[![Build Status](https://travis-ci.org/jaredledvina/sensu-client.svg?branch=master)](https://travis-ci.org/jaredledvina/sensu-client)
[![MIT Licensed](https://img.shields.io/badge/license-MIT-green.svg)](https://tldrlegal.com/license/mit-license)
[![Ansible Galaxy](https://img.shields.io/badge/role-jaredledvina.sensu--client-blue.svg)](https://galaxy.ansible.com/jaredledvina/sensu-client/)

Sensu Client
=========

Ansible role for Sensu Clients. Tested on Debian 8, Debian 9, and Ubuntu 14.04 only.

Requirements
------------

* Configured Sensu master server(s)

Role Variables
--------------

See [`defaults/main.yml`](https://github.com/jaredledvina/sensu-client/blob/defaults/vars/main.yml)

Dependencies
------------

Nothing at this time.

Example Playbook
----------------
```yaml
---
- hosts: client
  roles:
    - role: sensu-client
      sensu_client_gems:
        - sensu-plugin
      sensu_client_plugins:
        - sensu-plugins-process-checks
      sensu_client_checks:
        sensu-website:
          command: check-http.rb -u https://sensuapp.org
          subscribers:
            - all
          interval: 60
```


Development:
------------

This repo uses pre-commit to manage local git commit hooks. Checkout https://pre-commit.com for details.
