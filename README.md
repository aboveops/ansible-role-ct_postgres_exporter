aboveops.ct_postgres_exporter
=========

Postgres Exporter in docker container

Description
-----------

This role deploys a docker container with postgres exporter inside.

Example
-------

- hosts:
    - database
  become: true
  tags:
    - postgres-exporter
  roles:
    - role: aboveops.ct_postgres_exporter
      postgres_exporter_bind_ip: "{{ backnet_ip }}"
      postgres_exporter_port: '9187'
      postgres_exporter_database_ip: "{{ backnet_ip }}"
      postgres_exporter_database_port: "5432"
      postgres_exporter_base: "{{ psql_dbname }}"
      postgres_exporter_database_user: "{{ psql_user }}"
      postgres_exporter_database_password: "{{ psql_pass }}"

Install
-------

This role can be installed from [Ansible Galaxy](https://galaxy.ansible.com/):

`ansible-galaxy install aboveops.ct_postgres_exporter`

License
-------

MIT

Author Information
------------------

Anastasia Muinova, <nirvana@freehck.com>
Dmitrii Kashin, <freehck@freehck.com>
