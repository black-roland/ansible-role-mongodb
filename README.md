# Ansible Role: MongoDB

An Ansible role that installs MongoDB on Centos 7.x using SCL.

## Role Variables

Available variables are listed below, along with default values:

```yml
mongodb_version: 3.2
mongodb_mongod_conf_path: /etc/mongod.conf
mongodb_service: mongod
mongodb_systemLog_verbosity: 0
mongodb_systemLog_destination: file
mongodb_systemLog_path: /var/log/mongodb/mongod.log
mongodb_systemLog_logAppend: true
mongodb_systemLog_logRotate: reopen
mongodb_net_port: 27017
mongodb_net_bindIp: 127.0.0.1,::1
mongodb_net_ipv6: true
mongodb_net_unixDomainSocket_enabled: true
mongodb_net_unixDomainSocket_pathPrefix: /run/mongodb
mongodb_storage_dbPath: /var/lib/mongodb
```

## Example Playbook

```yml
- hosts: mongodb
  become: true
  roles:
    - { role: black-roland.ansible-role-mongodb }
```

## License

MIT
