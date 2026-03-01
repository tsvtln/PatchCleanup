# PatchCleanup

Minimal Ansible role and playbook to update the apt cache and autoremove unused packages.

## Output

The role prints a final task named "Job Summary Output" with a multi-line summary, including host, change status, and a list of removed packages if any. This is designed for both human readability and downstream parsing.

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
