# Ansible Labs

![](https://upload.wikimedia.org/wikipedia/commons/thumb/2/24/Ansible_logo.svg/200px-Ansible_logo.svg.png)

## Lab Environment

Ubuntu 22.04 LTS workstation with Ansible installed.

## Requirements

- All these labs are for ansible, your instructor will review UNIX commands with you before working on ansible
- Ansible uses `YAML` files, your instructor will cover and talk about how to create a yaml file with you
- At the time of writing this lab, there are over 3000 modules; we will only cover some of them as an example.

## Labs

### 1. Installation and Setup

- 1.1 [Setup ansible control center](setup/Install-Ansible.md)
- 1.2 [Setup inventory](setup/Configure-Inventory.md)

### 2. AdHoc

- 2.1 [Ping Hosts](adhoc/ping.md)
- 2.2 [Facts](adhoc/facts.md)
- 2.3 [File/folder manipulations](adhoc/file.md)
- 2.4 [APT](adhoc/apt.md)

### 3. Variables

- 3.1 [Basic Playbook](variable/vars/sample.yml)
- 3.2 [Variable in Playbook](variable/vars/sample.yml)
- 3.3 [Prompt the use](loop/sample.yml)
- 3.4 [Variables in external](loop/sample.yml)
- 3.5 [Set Fact](variable/set_fact/readme.md)
- 3.6 [Register Variable](variable/register/readme.md)

### 4. Condition

### 5. Loops

### 6. Handler

### 7. Blocks

### 8. Templates

### 9. Ansible Vault

### 10. Roles

- 3.2 - [Loop](playbook/loop/sample.yml)
- 3.3 - [Condition](playbook/condition/sample.yml)
- 3.4 - [Handler](playbook/handler/sample.yml)
- 3.5 - __Sample__: [Apache2](playbook/apache2)
- 3.6 - __Sample__: [LAMP](playbook/lamp/sample.yml)

* [Jinja2](jinja2/sample.yml)
* [Log per Host](extra/log_per_host/README.md)
* [Fact Caching](extra/fact_cache/README.md)

* __Sample__: [LAMP Role](role/lamp/site.yml)
* __Sample__: [Wordpress Role](role/wordpress/sites.yml)

