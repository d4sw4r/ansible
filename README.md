# ansible-skel

## setup
```
# create venv
python3.xx -m venv venv
# source venv
. venv/bin/activate
# install ansible and dependencies
pip install -r requirements.txt
# install ansible dependencies
ansible-galaxy install -r requirements.yml
```

## commands
```
# run ansible module
ansible -m ping  -i inventory/hosts.yml all
# run ad-hox command
ansible -a "ls -rthl"  -i inventory/hosts.yml all
# run playbook in check-mode
ansible-playbook site.yml -i inventory/hosts.yml --check --diff
# run playbook limited to one host in inventory
ansible-playbook site.yml -i inventory/hosts.yml -l <host>
# run playbook limited to one tag
ansible-playbook site.yml -i inventory/hosts.yml -t <tag>

```
