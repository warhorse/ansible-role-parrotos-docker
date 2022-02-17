Ansible Parrot OS (Docker)
=========
[![CI](https://github.com/warhorse/ansible-role-parrotos-docker/workflows/CI/badge.svg?event=push)](https://github.com/warhorse/ansible-role-parrotos-docker/actions?query=workflow%3ACI)
[![warhorse.parrotos_docker](https://img.shields.io/ansible/role/58075)](https://galaxy.ansible.com/warhorse/parrotos_docker)
[![warhorse.parrotos_docker](https://img.shields.io/ansible/quality/58075)](https://galaxy.ansible.com/warhorse/parrotos_docker)
[![warhorse.parrotos_docker](https://img.shields.io/ansible/role/d/58075)](https://galaxy.ansible.com/warhorse/parrotos_docker)
![License](https://img.shields.io/github/license/warhorse/ansible-role-parrotos-docker)
![Commit](https://img.shields.io/github/last-commit/warhorse/ansible-role-parrotos-docker)

![Parrot OS Logo](./images/parrot_os_logo.png "Parrot OS Logo")


Install Parrot OS (Docker)

This role is part of the Warhorse Automation Framework. This role can be used with Warhorse or as a standalone role.

Docker Image
-------------

Built in docker image.

Role Variables
--------------

A list of all the variables can be found in ./defaults/main.yml.

`parrotos_dir` - Parrot OS container directory

`parrotos_ports` - Parrot OS container ports

`parrotos_hostname` - Parrot OS container hostname

`parrotos_container_name` - Parrot OS container name

`parrotos_tz` - Parrot OS time zone

`parrotos_vnc_password` - Parrot OS VNC password

`parrotos_root_password` - Parrot OS root password

`parrotos_xuser_password` - Parrot OS xuser password

`parrotos_docker_network` Parrot OS container docker network


Dependencies
------------

```shell
ansible-galaxy install geerlingguy.docker geerlingguy.pip
```

Install
------------

```shell
ansible-galaxy install warhorse.parrotos_docker
```

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
      - { role: warhorse.parrotos_docker }
```

Example Vars
----------------

```yaml
parrotos_hostname: "parrotos"
parrotos_container_name: "parrotos"
parrotos_tz: "America/New_York"
parrotos_vnc_password: "password"
parrotos_root_password: "password"
parrotos_xuser_password: "password"
parrotos_docker_labels: {}
parrotos_docker_network: "parrotos"
parrotos_dir: '/opt/docker/parrotos'
parrotos_ports:
  - "0.0.0.0:80:6080"
```

License
-------

MIT/BSD

Author Information
------------------

Ralph May
