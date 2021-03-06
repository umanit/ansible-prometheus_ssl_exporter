# Ansible Role: ssl exporter

[![License](https://img.shields.io/badge/license-MIT%20License-brightgreen.svg)](https://opensource.org/licenses/MIT)
[![GitHub tag](https://img.shields.io/github/v/tag/umanit/ansible-prometheus_ssl_exporter)](https://github.com/umanit/ansible-prometheus_ssl_exporter/tags)

## Description

Deploy prometheus [Ribbybibby ssl_exporter](https://github.com/ribbybibby/ssl_exporter) using ansible.

Ribbybibby ssl_exporter allow to monitor independently each certifacte of the chain (unlike blackbox_exporter) 


## Notes

Role forked and largely inspired by [Cloudalchemy Blackbox Exporter Ansible role](https://github.com/cloudalchemy/ansible-blackbox-exporter)

Role is supposed to work with Debian, Suse, RedHat, Fedora, (See [Ansible Galaxy meta](/meta/main.yml)), but it was only tested on Ubuntu Bionic (18.04).

## Requirements

- Ansible >= 2.7 (It might work on previous versions, but we cannot guarantee it)

## Role Variables

All variables which can be overridden are stored in [defaults/main.yml](defaults/main.yml) file.

Only two are defined: 
* ssl_exporter_version: version of ssl_exporter to install
* ssl_exporter_web_listen_address: IP and port to listen

All other flags used by ssl_exporter can be defined by ssl_exporter_cli_flags variable. 

## Example

### Playbook

Use it in a playbook as follows:
```yaml
- hosts: all
  roles:
    - umanit.prometheus_ssl_exporter
```
## License

This project is licensed under MIT License. See [LICENSE](/LICENSE) for more details.
