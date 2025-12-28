# Ansible

A collection of more or less polished Ansible roles for automation of various Debian-based services.

## Configuration

The inventories directory contains folders of companies/projects, in which you will find a hosts file where you can add hostnames of your servers. The host_vars directory is used for specifying host-specific variables (e.g. Proxmox API Keys).

Configure role-based variables in roles/x/vars/main.yml. You can also override them by including them in the host_vars.

## Structure

Keeping it as simple as possible, the playbooks directory simply runs roles from the roles directory.

## Usage

Run `ansible-playbook -i inventories/example proxmox.yml` to run the Proxmox role.
