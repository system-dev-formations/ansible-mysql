# Ansible MySQL Role
-------

This is an Ansible role that will provision a fresh mysql/mariadb server installation.

<br>

## More Documentation
-------
[clusterfrak.com](http://clusterfrak.com/devops/ansible/ansible_mysql/)

<br>

## Requirements
-------

__1. &nbsp;&nbsp; Install dependencies:__ <br>

> RedHat based distros (RHEL, CentOS):

```bash
sudo yum -y install epel-release
sudo yum clean all
sudo yum -y install ansible
```

<br>

__3. &nbsp;&nbsp; Create directory structure:__ <br>

Create the directory structure that you are going to use. In this tutorial we are going to set up ansible roles in __/etc/ansible/roles__

<br>

```bash
mkdir -p /etc/ansible/roles || exit 0
```
<br>

__4. &nbsp;&nbsp; Set ansible host:__

Set Ansible localhost entry so that ansible knows it will run against localhost and can talk to itself on localhost without attempting to open a TCP socket connection. 

<br>

```bash
echo localhost ansible_connection=local > /etc/ansible/hosts
```

<br>

## Dependencies
-------

No other roles required in order to run this role

<br>

## Example Playbook With Default Values
-------

This playbook will set up MySQL/Mariadb, it will deploy and maintain the my.conf and file. It will set the my.conf file to listen on the default IP address instead of localhost.

    - hosts: mysql-servers
      become: true
     roles:
       - clusterfrak.mysql

## License
-------

BSD

## Author Information
-------

[Rich Nason](http://nason.co) <br>
[Clusterfrak Doc Site](http://clusterfrak.com) <br>
[Container Doc Site](http://appcontainers.com) <br>

