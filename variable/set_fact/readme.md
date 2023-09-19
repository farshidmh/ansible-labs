# Ansible Playbook: Setting and Using Facts

## Duration

Approximately 20 minutes

## Objective

The objective of this lab is to explore the use of the `set_fact` module in an Ansible playbook. This lab will guide you through the process of defining facts dynamically during playbook execution and referencing them in subsequent tasks.

## Prerequisites:

- Basic understanding of Ansible.
- Ansible installed on your machine.
- Access to target hosts in the `webservers` inventory group.

## Step-by-step guide:

### Step A: Set up the Ansible Playbook

1. Create a new YAML file named `facts_playbook.yml`.
2. Specify the play's name, target hosts, and whether to gather facts or not.

```yaml
- name: A play with variables
  hosts: webservers
  gather_facts: no
```

### Step B: Define Facts Using `set_fact` Module

3. Within the tasks, create the first task to define three new facts (`fact_one`, `fact_other`, and `john_fact`) using the `set_fact` module.

```yaml
  tasks:
    - name: Setting host facts using set_fact module
      set_fact:
        fact_one: "Hello"
        fact_other: "Bye"
        john_fact: "Doe"
```

### Step C: Utilize Facts in Tasks

4. Create a task to print the value of the `john_fact`.

```yaml
    - name: Print some facts
      debug:
        var: john_fact
```

5. Create another task to print the value of the `fact_other`. Note that there's a typo in the variable name provided ("fact_othert"), so make sure to correct it.

```yaml
    - name: Print some facts
      debug:
        var: fact_other
```

### Step D: Execute the Playbook

6. Save the `facts_playbook.yml` file.
7. Run the playbook using the following command:

```
ansible-playbook -i your_inventory_file.ini facts_playbook.yml
```

Replace `your_inventory_file.ini` with the path to your inventory file if you're not using the default inventory.

## Final File

You can compare your playbook with the [facts_playbook.yml](facts_playbook.yml) file in the current directory.

## Summary

This lab provided a hands-on approach to working with the `set_fact` module in Ansible. We dynamically set facts during the playbook's execution and utilized them in subsequent tasks. Using facts, you can store specific information about a host and leverage it for various automation tasks.