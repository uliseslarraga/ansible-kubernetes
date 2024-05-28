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
ansible-inventory -i inventory.ini --list
```
Testing group nodes 
```
ansible kube-adm,kube-workers -m ping -i inventory.ini
```

## Running a playbook

You can execute a playbook with the following command. We have added the -K flag to supply root password to provisioning some configuration files in system folders as root user

```
ansible-playbook -i inventory.yml -K playbooks/setup-ctrl-plane.yml
```