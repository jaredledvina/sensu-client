Sensu Client
=========

Ansible role for Sensu Clients. Tested on Debian 8 only. 

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
           sensu_client_rabbitmq_host: mycoool.rabbotmq.host.com
           

License
-------

TBD


