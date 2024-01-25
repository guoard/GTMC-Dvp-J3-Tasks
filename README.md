# Ansible Playbook Execution Guide

## Overview

This guide provides instructions for executing an Ansible playbook to deploy and configure a WordPress environment. The playbook automates various tasks.

## Prerequisites

Ensure the following prerequisites are met before running the Ansible playbook:

1. Ansible Installed: Make sure Ansible is installed on the machine from which you plan to run the playbook.

2. Ansible Playbook and Inventory Files: The playbook file (playbook.yaml) and the inventory file (hosts.yaml) must be present in the same directory where you execute the Ansible command.

## Running the Ansible Playbook

To execute the Ansible playbook, use the following command:

```bash
ansible-playbook playbook.yaml -i hosts.yaml --diff --ask-become-pass
```

- playbook.yaml: The main Ansible playbook file containing the tasks and roles.
- hosts.yaml: The inventory file specifying the target hosts.

The --diff option displays the differences in configuration files before and after changes. The --ask-become-pass option prompts for the sudo password to escalate privileges.

## Exclusions

The following tasks are not implemented in this playbook:

1. Backup of WordPress Database and Registry: Backing up the WordPress database and registry is not included.

2. Limited Hardening: The playbook provides basic configurations and does not extensively focus on system hardening.
