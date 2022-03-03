# ansible-role-kubeadm

![Ansible](https://github.com/avnes/ansible-role-kubeadm/actions/workflows/ansible.yaml/badge.svg)

Ansible role for installing kubeadm.

## Requirements

Poetry. Install it from <https://python-poetry.org/docs/>

## Role Variables

```yaml
kubeadm_version: latest     # It can also be a specifik version like v1.21.4
kubeadm_for_all_users: true # If false it will install in in the users ~/bin directory
command_shell: bash         # Must be bash or zsh
```

## Dependencies

None

## Example Playbook

```yaml
- hosts: all
  roles:
     - { role: avnes.kubeadm }
```

## For pip compability

```bash
poetry export --dev --output requirements.txt
```

## Test

```bash
poetry install
poetry shell
molecule test
```

## License

MIT

## Author Information

<https://github.com/avnes>
