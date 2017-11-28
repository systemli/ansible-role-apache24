# ansible-role-apache24

[![Build Status](https://travis-ci.org/systemli/ansible-role-apache24.svg?branch=master)](https://travis-ci.org/systemli/ansible-role-apache24) [![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-apache24-blue.svg)](https://galaxy.ansible.com/systemli/apache24/)

Install and configure Apache 2.4

## Role Variables

    apache24_packages:
      - apache2
      - apache2-utils
      - python-passlib

    apache24_http_port: 80
    apache24_https_port: 443
    # port or ip:port
    apache24_additional_ports: []

    apache24_custom_modules:
      - expires.conf
      - deflate.conf
      - headers.conf
      - proxy.conf
      - status.conf

    apache24_custom_configs:
      - security.conf
      - other-vhosts-access-log.conf
      - httpoxy.conf

    apache24_modules:
      - actions
      - alias
      - auth_basic
      - authn_file
      - authz_groupfile
      - authz_host
      - authz_user
      - autoindex
      - cache
      - cgid
      - deflate
      - dir
      - env
      - expires
      - headers
      - mime
      - negotiation
      - proxy
      - proxy_http
      - proxy_wstunnel
      - reqtimeout
      - rewrite
      - setenvif
      - ssl
      - status
      - authz_host
      - filter
      - cache_disk
      - socache_shmcb

    apache24_disabled_modules: []

    apache24_mpm_worker: True
    apache24_mpm_startservers: 2
    apache24_mpm_serverlimit: 16
    apache24_mpm_minsparethreads: 25
    apache24_mpm_maxsparethreads: 75
    apache24_mpm_threadlimit: 64
    apache24_mpm_threadperchild: 25
    apache24_mpm_max_clients: 150
    apache24_mpm_maxrequestworkers: 1000
    apache24_mpm_maxconnectionsperchild: 0

    # source https://weakdh.org/sysadmin.html
    apache24_ssl_cipher_suite: ECDHE-RSA-AES128-GCM-SHA256:ECDHE-ECDSA-AES128-GCM-SHA256:ECDHE-RSA-AES256-GCM-SHA384:ECDHE-ECDSA-AES256-GCM-SHA384:DHE-RSA-AES128-GCM-SHA256:DHE-DSS-AES128-GCM-SHA256:kEDH+AESGCM:ECDHE-RSA-AES128-SHA256:ECDHE-ECDSA-AES128-SHA256:ECDHE-RSA-AES128-SHA:ECDHE-ECDSA-AES128-SHA:ECDHE-RSA-AES256-SHA384:ECDHE-ECDSA-AES256-SHA384:ECDHE-RSA-AES256-SHA:ECDHE-ECDSA-AES256-SHA:DHE-RSA-AES128-SHA256:DHE-RSA-AES128-SHA:DHE-DSS-AES128-SHA256:DHE-RSA-AES256-SHA256:DHE-DSS-AES256-SHA:DHE-RSA-AES256-SHA:AES128-GCM-SHA256:AES256-GCM-SHA384:AES128-SHA256:AES256-SHA256:AES128-SHA:AES256-SHA:AES:CAMELLIA:DES-CBC3-SHA:!aNULL:!eNULL:!EXPORT:!DES:!RC4:!MD5:!PSK:!aECDH:!EDH-DSS-DES-CBC3-SHA:!EDH-RSA-DES-CBC3-SHA:!KRB5-DES-CBC3-SHA

## Download

Download latest release with `ansible-galaxy`

	ansible-galaxy install systemli.apache24

## Example Playbook

```
    - hosts: servers
      roles:
         - { role: systemli.apache24 }
```

## License

GPL

## Author Information

https://www.systemli.org