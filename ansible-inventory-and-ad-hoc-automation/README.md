# Ansible Inventory Management and Ad-hoc Automation

## What This Does

This implementation demonstrates foundational infrastructure automation using Ansible. It establishes inventory-driven host management, validates connectivity between control and managed systems, executes administrative operations through Ansible modules, and performs common infrastructure tasks without requiring agents on target hosts.

The solution showcases Ansible's push-based automation model and provides a reusable structure for managing servers through inventories, modules, and command execution workflows.

## Architecture

```text
+----------------------+
|   Control Node       |
|  CentOS Stream 9     |
|  Ansible Core        |
+----------+-----------+
           |
           | Inventory
           |
+----------v-----------+
|     Ansible Core     |
|   Modules Engine     |
+----------+-----------+
           |
           |
  +--------+--------+
  |                 |
  v                 v
+------+       +---------+
| Web  |       | Database|
|Hosts |       | Hosts   |
+------+       +---------+
```

## Prerequisites

* CentOS Stream 9, RHEL 9, Rocky Linux 9, or equivalent
* Python 3
* Ansible Core
* SSH access to managed systems
* Administrative privileges for package and service operations

## Setup & Installation

```bash
sudo dnf install -y ansible-core
```

Verify installation:

```bash
ansible --version
ansible-inventory --version
```

## How to Reproduce

1. Create an Ansible inventory file.
2. Define host groups and connection methods.
3. Validate inventory structure.
4. Test host connectivity using the ping module.
5. Gather system facts.
6. Execute shell commands through Ansible modules.
7. Perform file management operations.
8. Install packages using package modules.
9. Manage services through Ansible automation.

## Tools Used

* Ansible Core
* INI Inventory
* YAML Inventory
* SSH
* DNF
* Linux Shell
* Systemd

## Key Skills Demonstrated

* Infrastructure automation
* Inventory design and management
* Agentless configuration management
* Remote command execution
* Linux administration through Ansible
* Service management automation
* Package lifecycle management
* Host grouping and targeting strategies

## Real-World Use Case

Organizations use Ansible to manage fleets of Linux servers from a centralized control node. Infrastructure teams rely on inventories, modules, and automation workflows to perform updates, configuration changes, package deployments, compliance checks, and operational tasks consistently across large environments.

## Lessons Learned

* Inventory design directly affects automation scalability.
* Ansible modules are preferred over raw shell commands whenever possible.
* Host grouping simplifies large-scale administration.
* Agentless automation reduces operational complexity.
* Fact gathering provides valuable infrastructure visibility.

## Troubleshooting Log

### Inventory User Mismatch

The original inventory examples used an Ubuntu-specific user account. The environment used CentOS, requiring the inventory user to be updated accordingly.

### Package Manager Modernization

Legacy installation guidance relied on older package-management practices. The environment supported modern Ansible Core installation through current repositories.

### Service Name Differences

Service naming varies across distributions. Verification was performed before managing services to ensure the correct systemd unit name was used.

### Localhost Multi-Host Testing

Additional inventory adjustments were required when simulating multiple hosts on a single machine using local connections.

