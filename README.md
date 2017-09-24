[![CircleCI](https://img.shields.io/circleci/project/github/jaredledvina/sensu-client.svg)](https://circleci.com/gh/jaredledvina/sensu-client)
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

See `vars/main.yml`

Dependencies
------------

Nothing at this time.

Example Playbook
----------------

    - hosts: client
      roles:
         - sensu-client
           sensu_client_rabbitmq_host: mycoool.rabbitmq.host.com


Development:
------------

This repo uses pre-commit to manage local git commit hooks. Checkout https://pre-commit.com for details.
