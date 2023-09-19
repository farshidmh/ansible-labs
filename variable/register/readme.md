# Using the `register` Keyword

## Duration

Approximately 20 minutes

## Objective

The objective of this lab is to demonstrate the use of the `register` keyword in an Ansible playbook. Through this lab, you will learn how to capture the output of a command or module into a variable and then utilize that variable in subsequent tasks.

## Prerequisites:

- Basic understanding of Ansible.
- Ansible installed on your machine.
- Access to target hosts in the `webservers` inventory group.
- A file named `a.txt` located in `/home/ubuntu/` on the target host(s) with test data.

## Step-by-step guide:

### Step A: Set up the Ansible Playbook

- Create a new YAML file named `register_playbook.yml`.
- Specify the play's name, target hosts, and the decision to avoid gathering facts.

```yaml
- name: A play with register
  hosts: webservers
  gather_facts: no
```

### Step B: Registering Command Output into a Variable

Create a task that uses the `shell` module to read the contents of `/home/ubuntu/a.txt` on the target host. Use the `register` keyword to store the command's output in a variable named `motd_contents`.

```yaml
  tasks:
    - name: Register a variable
      shell: cat /home/ubuntu/a.txt
      register: motd_contents
```

### Step C: Utilize the Registered Variable

Create a subsequent task to print the contents of the registered variable. The stdout attribute of the registered variable contains the actual output of the command.

```yaml
    - name: print the variable
      debug:
        msg: "{{ motd_contents.stdout }}"
```

### Step D: Execute the Playbook

- Save the `register_playbook.yml` file.
- Run the playbook using the following command:

```
ansible-playbook register_playbook.yml
```

## Final File

You can compare your playbook with the [register_playbook.yml](register_playbook.yml) file in the current directory.


## Summary

In this lab, we delved into the `register` keyword's functionality in Ansible. By capturing command outputs or results from other modules, `register` allows for dynamic and adaptive playbook designs. You can then use the registered variable to make decisions, print outputs, or pass information to
other tasks and roles.