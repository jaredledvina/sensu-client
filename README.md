[![CircleCI](https://img.shields.io/circleci/project/github/jaredledvina/sensu-client.svg)](https://circleci.com/gh/jaredledvina/sensu-client)
[![MIT Licensed](https://img.shields.io/badge/license-MIT-green.svg)](https://tldrlegal.com/license/mit-license)

Sensu Client
=========

Ansible role for Sensu Clients. Tested on Debian 8, Debian 9, and Ubuntu 14.04 only.

Requirements
------------

* Configured Sensu master server(s)
* Requires SSL cert/key pair trusted by the RabbitMQ server.
* Use `sensu_client_rabbitmq_ssl_cert` and `sensu_client_rabbitmq_ssl_key`

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


License
-------

TBD


Development:
------------

This repo uses pre-commit to manage local git commit hooks. Checkout https://pre-commit.com for details.
