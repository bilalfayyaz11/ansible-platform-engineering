# Ansible Role-Based Automation

This project demonstrates role-based automation using Ansible on a RHEL-compatible Linux environment.

## What This Project Covers

- Custom Ansible role creation using `ansible-galaxy init`
- Standard role directory structure
- Role defaults and variables
- Task organization
- Jinja2 template deployment
- Service handlers
- Role metadata
- Role dependency management
- Local inventory execution
- Web server validation using Ansible and curl

## Roles

### common

The `common` role prepares the baseline platform environment by installing common utilities and creating an operations directory.

### webserver

The `webserver` role installs and configures Apache HTTP Server. It also deploys a templated index page, starts the required services, and opens the HTTP firewall port.

The `webserver` role depends on the `common` role.

## Project Structure

```text
ansible-role-based-automation/
├── ansible.cfg
├── inventory/
├── outputs/
├── playbooks/
├── roles/
│   ├── common/
│   └── webserver/
└── README.md
