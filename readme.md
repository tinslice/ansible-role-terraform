# ansible-role-terraform

Ansible role for installing terraform

## Usage

Install role

```bash
ansible-galaxy install -f -r requirements.yml -p roles/
```

Install Terraform

```bash
ansible-playbook playbook.yml --ask-become-pass
```

UnInstall Terraform

```bash
ansible-playbook playbook.yml --ask-become-pass --tags remove
```

### Example configuration

Example 'requirements.yml'

```yaml
---
- name: terraform
  src: https://github.com/tinslice/ansible-role-terraform.git
```

Example 'playbook.yml'

```yaml
---
- hosts:
    - localhost
  connection: local
  become: yes
  vars:
    terraform_version: 0.14.5
  roles:
    - role: terraform
```


