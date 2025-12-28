# Ansible

A collection of more or less polished Ansible roles for automation of Debian, Proxmox and Docker-based services.

## Configuration

The inventories directory contains folders of companies/projects, in which you will find a hosts file where you can add hostnames of your servers. The host_vars directory is used for specifying host-specific variables (e.g. Proxmox API Keys).

Configure role-based variables in roles/x/vars/main.yml. You can also override them by including them in the host_vars.

## Structure

Keeping it as simple as possible, the playbooks in the root directory simply run roles from the roles directory.

Docker projects are created in /srv by default. You can change the tasks if you wish to use /opt or other directories.

## Usage

Run `ansible-playbook -i inventories/example proxmox.yml` to run the Proxmox role.
