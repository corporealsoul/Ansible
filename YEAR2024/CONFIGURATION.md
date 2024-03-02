### Creating a working directory,

`[anup@rhel-92-104 ~]$ ls -ltr /etc/ansible`

`[anup@rhel-92-104 ~]$ sudo nano /etc/ansible/hosts`

    [controller]
    192.168.56.104  ansible_ssh_user=anup   ansible_ssh_pass= # Host address, user_name and password
    
    [worker]
    192.168.56.108  ansible_ssh_user=anup   ansible_ssh_pass= # Host address, user_name and password

`[anup@rhel-92-104 ~]$ ansible-inventory --list`

<br>

