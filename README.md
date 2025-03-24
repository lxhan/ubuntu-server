# Ubuntu Server Ansible Playbooks

Ansible playbooks for setting up and configuring Ubuntu servers in home and office environments.

## Structure

- `inventory/`: Server inventory and group variables
- `playbooks/`: Main playbooks for different aspects of configuration
- `roles/`: Reusable roles for server setup

## Included Roles

- `common`: Basic server setup and packages
- `security`: SSH hardening and security configuration
- `node`: Node.js installation via NVM

## Usage

### Basic Server Setup

```bash
ansible-playbook playbooks/site.yml
```

### Target Specific Environments

```bash
ansible-playbook playbooks/site.yml --limit home -K
ansible-playbook playbooks/site.yml --limit office -K
```

### Run Only Specific Tasks

```bash
ansible-playbook playbooks/site.yml --tags security
```

## Requirements

- Ansible 2.9+
- SSH access to target servers
