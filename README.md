# K3s cluster maintenance playbooks
This is a simple repo to automate k3s nodes maintenance tasks using ansible playbooks.

## Commands
### Ping
Ping the ssh connection using the provided user in the inventory. Will ask for password through the terminal.

`ansible all -m ping -i inventory.ini --ask-pass`

### Run playbook
Runs playbook.yaml. Will ask for ssh password for the provided user in the inventory file, as well as the privilege escalation password.

`ansible-playbook -vv -i inventory.ini playbook.yaml --ask-pass --ask-become-pass`