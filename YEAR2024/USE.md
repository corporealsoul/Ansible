
### Checking communication,

`[anup@rhel-92-104 ~]$ ansible localhost -m ping`

`[anup@rhel-92-104 ~]$ ansible all -m ping`

`[anup@rhel-92-104 ~]$ ansible controller -m ping`

`[anup@rhel-92-104 ~]$ ansible worker -m ping`

`[anup@rhel-92-104 ~]$ ansible-inventory --list`

`[anup@rhel-92-104 ~]$ ansible 192.168.56.108 -m ping`

`[anup@rhel-92-104 ~]$ ansible -i /etc/ansible/hosts controller -m ping`

<br>

### Run a playbook,

`[anup@rhel-92-104 ~]$ cd /etc/ansible/`

`[anup@rhel-92-104 ansible]$ ls -ltr`

`[anup@rhel-92-104 ansible]$ sudo mkdir playbook`

`[anup@rhel-92-104 ansible]$ cd playbook/`

`[anup@rhel-92-104 playbook]$ sudo nano gather_facts.yml`

    ---
    - name: Gathering Facts
      hosts: all
    #  hosts: controller
    #  hosts: worker
      gather_facts: yes
    ...

`[anup@rhel-92-104 playbook]$ ansible-playbook gather_facts.yml --check`

`[anup@rhel-92-104 playbook]$ ansible-playbook -i /etc/ansible/hosts gather_facts.yml --check`

`[anup@rhel-92-104 playbook]$ ansible-playbook -l controller gather_facts.yml --check`

<br>