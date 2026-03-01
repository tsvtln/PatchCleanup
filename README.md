# PatchCleanup

Minimal Ansible role and playbook to update the apt cache and autoremove unused packages.

## Output

The role prints a final task named "Job Summary Output" so downstream tooling can parse results. The autoremove task also emits the full Ansible result for visibility.

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
