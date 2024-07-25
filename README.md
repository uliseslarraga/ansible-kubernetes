# Ansible getting started 

The present repo is a full list of ansible examples
# Requirements
- Python 
- ansible 

## Installing ansible 
```
pip install ansible
```

## Veryfing inventory
```
ansible-inventory -i inventory.yml --list
```
Testing group nodes 
```
ansible master,workers -m ping -i inventory.yml
```

## Running a playbook

You can execute a playbook with the following command. We have added the -K flag to supply root password to provisioning some configuration files in system folders as root user

```
ansible-playbook -i inventory.yml -K playbooks/setup-ctrl-plane.yml
```