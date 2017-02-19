# Ansible Role Influxdb

Install and configure InfluxDB.

Actually only work on Debian 8.

# Variables

All variables listed in defaults/main.yaml

## Example Playbook

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
