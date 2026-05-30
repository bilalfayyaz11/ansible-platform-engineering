# Inventory Management Automation

This project demonstrates Ansible inventory management for multi-environment infrastructure automation.

## What This Project Covers

- Static inventory design
- Development and production inventory separation
- Host-specific variables using `host_vars`
- Group-level configuration using `group_vars`
- Parent and child inventory groups
- Variable precedence testing
- Dynamic host grouping with `group_by`
- Inventory validation using `ansible-inventory`

## Project Structure

```text
inventory-management-automation/
├── group_vars/
├── host_vars/
├── inventories/
├── outputs/
├── playbooks/
├── inventory.ini
├── inventory-dev.ini
├── inventory-prod.ini
└── README.md
