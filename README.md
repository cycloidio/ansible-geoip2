# ansible-geoip2

# Ansible Role: geoip2

[![Build Status](https://travis-ci.org/cloudalchemy/ansible-fluentd.svg?branch=master)](https://travis-ci.org/cloudalchemy/ansible-fluentd)
[![License: MIT](https://img.shields.io/badge/license-MIT%20License-brightgreen.svg)](https://opensource.org/licenses/MIT)
[![Ansible Role](http://img.shields.io/badge/ansible%20role-cloudalchemy.fluentd-blue.svg)](https://galaxy.ansible.com/cloudalchemy/fluentd/)
[![GitHub tag](https://img.shields.io/github/tag/cloudalchemy/ansible-fluentd.svg)](https://github.com/cloudalchemy/ansible-fluentd/tags)

## Description

Install GeoIP2 City Base de données | MaxMind.
Nginx geoip2 (MaxMind) module is not packaged by default in debian. Use this role as a workaround.

To correctly compile nginx module we suggest to use official nginx repo as source.

## Requirements


## Role Variables

All variables which can be overridden are stored in [defaults/main.yml](defaults/main.yml) file as well as in table below.

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `geoip_packages_dependancies` | [] | dependancies packages |

## Example

### Playbook

Use it in a playbook as follows:
```yaml
- hosts: all
  become: true
  roles:
    - cycloid.geoip2
```

If used with jdauphant.nginx we suggest to execute geoip2 role after and defined the following variable
```yaml
# started by geoip2 role
nginx_official_repo: True

# Use the latest nginx stable
nginx_start_service: false
```

## License

This project is licensed under MIT License. See [LICENSE](/LICENSE) for more details.
