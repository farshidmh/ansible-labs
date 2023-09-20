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
- 3.3 [Prompt the use](loop/with_items/item_iteration.yml)
- 3.4 [Variables in external](loop/with_items/item_iteration.yml)
- 3.5 [Set Fact](variable/set_fact/readme.md)
- 3.6 [Register Variable](variable/register/readme.md)

### 4. Condition

- 4.1 [Basic](condition/basic/readme.md)
- 4.2 [Cast variables](condition/cast/readme.md)
- 4.3 [Complex](condition/complex/readme.md)
- 4.4 [Assert](condition/assert/readme.md)
- 4.5 [Challenge](condition/challenge/readme.md)

### 5. Loops

- 5.1 [With_items](loop/with_items/item_iteration.yml)
- 5.2 [Loop](loop/loop/readme.md)
- 5.3 [Loop with external variable](loop/loop_var/readme.md)
- 5.4 [Loop external task file](loop/loop_task/readme.md)

### 6. Handler

- 6.1 [Handler](handler/readme.md)

### 7. Blocks

- 7.1 [Block](block/simple/readme.md)

### 8. Templates

- 8.1 [Template](template/basic/readme.md)

### 9. Ansible Vault

- 9.1 [Vault](vault/readme.md)

### 10. Roles

- 10.1 [Roles](role/readme.md)


