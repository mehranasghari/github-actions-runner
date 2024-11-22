## Overview

This Ansible role simplifies the process of setting up a self-hosted GitHub Actions runner. It automates downloading, verifying, and configuring the runner to work with your specified GitHub repository.

## Requirements

- Ansible 2.9 or higher
- Access to the target machine(s) where the runner will be installed
- Internet connectivity on the target machine
- GitHub Personal Access Token with permissions to manage self-hosted runners

## Role Variables

- `github_repo_owner`: The GitHub username or organization name owning the repository in `role/github-actions-runner/vars/main.yml`.
- `github_repo_name`: The name of the GitHub repository where the runner will be registered `role/github-actions-runner/vars/main.yml`.
- `github_personal_access_token`: Your GitHub Personal Access Token with appropriate permissions in `role/github-actions-runner/vars/secrets.yml`. The `secrets.yml` file should be generated with `ansible-vault encrypt secrets.yml`. 

## Usage

Run the Ansible playbook:
```bash
ansible-playbook playbook.yml
```
If you encrypted secret.yml, include the --ask-vault-pass option:
```bash
ansible-playbook playbook.yml --ask-vault-pass
```
