# MySQL Ansible Role

## Overview

This Ansible project installs MySQL on Ubuntu and Red Hat Enterprise Linux (RHEL) servers using an Ansible role.

The role automatically detects the operating system and runs the appropriate installation tasks.

## Supported Operating Systems

* Ubuntu
* Red Hat Enterprise Linux (RHEL 10)

## Project Structure

```text
my-sql/
├── ansible.cfg
├── inventory
├── site.yml
└── roles/
    └── my-sql/
        ├── README.md
        └── tasks/
            ├── main.yml
            ├── ubuntu.yml
            └── redhat.yml
```

## How It Works

The playbook targets the `mysql_servers` group from the inventory.

The role checks the operating system family:

* Debian/Ubuntu → `ubuntu.yml`
* RedHat/RHEL → `redhat.yml`

Ubuntu uses the `apt` package manager, while RHEL uses the `dnf` package manager.



## Purpose

This project demonstrates the use of an Ansible role to automate MySQL installation on different Linux distributions using OS-specific tasks and package managers.
