# Ansible role: OS upgrade

[![Build Status](https://travis-ci.org/kamikazestar/ansible-role-os-upgrade.svg?branch=master)](https://travis-ci.org/kamikazestar/ansible-role-os-upgrade)

This role will upgrade your operating system to newest available version.

## Requirements

Currently this role don't require other roler or libralies.

## Role Variables

Role is using two variables:

  - debian_upgrade_type
  - debian_autoremove

They dedicated to Debian-based operating systems. First of them is used to choose type of the upgrade and available options  are:

  - dist
  - full
  - no
  - safe
  - yes

Secondone had been used to set autoremove behaviour and there are available only two options:

  - yes
  - no

For more details please read [Ansible apt module documentation](https://docs.ansible.com/ansible/latest/modules/apt_module.html#apt-module).


## Dependencies

This role currently don't have any dependencies itself, but for automated tests it's using [Jeff Geerling](https://hub.docker.com/u/geerlingguy/) Docker containers:

  - [docker-centos8-ansible](https://hub.docker.com/r/geerlingguy/docker-centos8-ansible/)
  - [docker-centos7-ansible](https://hub.docker.com/r/geerlingguy/docker-centos7-ansible/)
  - [docker-fedora31-ansible](https://hub.docker.com/r/geerlingguy/docker-fedora31-ansible/)
  - [docker-fedora30-ansible](https://hub.docker.com/r/geerlingguy/docker-fedora30-ansible/)
  - [docker-amazonlinux2-ansible](https://hub.docker.com/r/geerlingguy/docker-amazonlinux2-ansible/)
  - [docker-ubuntu1804-ansible](https://hub.docker.com/r/geerlingguy/docker-ubuntu1804-ansible/)
  - [docker-ubuntu1604-ansible](https://hub.docker.com/r/geerlingguy/docker-ubuntu1604-ansible/)
  - [docker-debian10-ansible](https://hub.docker.com/r/geerlingguy/docker-debian10-ansible/)
  - [docker-debian9-ansible](https://hub.docker.com/r/geerlingguy/docker-debian9-ansible/)

## Example Playbook

To use this role firstly you need to install them using command 'ansible-galaxy'. Then you can use this role in yours playbooks like below:

    - hosts: servers
      roles:
         - { role: kamikazestar.ansible-role-os-upgrade }

## License

This project is licensed under the MIT License - see the [LICENSE](https://github.com/kamikazestar/VagrantLab/blob/master/LICENSE) for details.

## Author Information

* **Marcin Slabonski** - *Initial work* - [kamikazestar](https://github.com/kamikazestar)

