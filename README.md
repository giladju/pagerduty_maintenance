# Pagerduty - bringing service in and out of maintenance mode 

## Required variables from inventory

* `vault_pagerduty_api_key`
* `vault_pagerduty_email`
* `vault_pagerduty_service`
* `env_name`

## Example playbook

```
---
- hosts: localhost
  roles: 
    - pagerduty_maintenance
```

## Example `ansible-playbook` commands

### Maintenance window ON

```
ansible-playbook playbooks/local-toggle-pagerduty-maintenance-mode.yml -e "in_maintenance=ON"
```

### Maintenance window OFF

```
ansible-playbook playbooks/local-toggle-pagerduty-maintenance-mode.yml -e "in_maintenance=OFF"
```