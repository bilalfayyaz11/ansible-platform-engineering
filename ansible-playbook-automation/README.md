# Ansible Playbook Automation for Web and Database Services

## What This Does

This implementation demonstrates infrastructure automation using Ansible playbooks. The solution automates web server deployment, database service configuration, package installation, service lifecycle management, configuration enforcement, and idempotency validation.

The automation is written using Infrastructure as Code principles and can be executed repeatedly while maintaining a predictable system state.

## Architecture

```text
+--------------------------------------------------+
|                 Control Node                     |
|              Ansible Core Engine                 |
+------------------------+-------------------------+
                         |
                         |
              Inventory Driven Execution
                         |
     +-------------------+-------------------+
     |                                       |
     v                                       v
+-------------+                     +---------------+
| Web Servers |                     | DB Servers    |
| Apache      |                     | MariaDB       |
| HTTPD       |                     | Configuration |
+-------------+                     +---------------+
