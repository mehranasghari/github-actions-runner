# GitHub Actions Runner Role

This role deploys a GitHub Actions runner on a target host.

## Requirements

- Ansible 2.9 or higher
- GitHub Personal Access Token with appropriate permissions

## Role Variables

See `defaults/main.yml` and `vars/main.yml` for configurable variables.

## Usage

Include the role in your playbook:

```yaml
- hosts: localhost
  roles:
    - github_actions_runner