Ansible Role InfluxDB
=========

Install and configure InfluxDB with admin,user,base and grant management

Actually only work on Debian 8.

Requirements
------------

None

Role Variables
--------------

All variables listed in defaults/main.yaml

Dependencies
------------

None

Example Playbook
----------------

    - hosts: influxdb
      vars:
        - influxdb_dir: "/app/influxdb"
        - influxdb_admin_users:
                - user: "admin"
                  pass: "xxxx"
        - influxdb_users:
                - user: "collectd"
                  pass: "xxxx"
        -  influxdb_databases:
                - collectd
      roles:
        - ansible-role-influxdb

License
-------

BSD

Author Information
------------------

David KULAK
