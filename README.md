# PatchCleanup

Minimal Ansible role and playbook to update the apt cache and autoremove unused packages.

## Usage

Run the playbook locally or in CI:

```bash
ansible-playbook -i localhost, -c local main.yml
```

Use tags to run only one step:

```bash
ansible-playbook -i localhost, -c local main.yml --tags update
ansible-playbook -i localhost, -c local main.yml --tags autoremove
```
