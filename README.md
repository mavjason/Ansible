# Ansible
Ansible Advanced- Hands-On - DevOps

This project automates this github repository: https://github.com/mmumshad/simple-webapp

Requirements:
  In the same Network:
  1)Virtual Controller with Ansible installed (example: 92.168.56.75) (Ubuntu 20.04 used)
  2)Virtual Target (example: 192.168.56.101) (Ubuntu 20.04 used)
  
Configure the inventory file:
    Set the correct:
     1) ansible_host (Ip of the Target) 
     2) ansible_user  (User) 
     3) ansible_password (password to ssh to User)
     
Run the following command:
    ansible-playbook playbook.yml -i inventory.txt --extra-vars "ansible_sudo_pass={root_password}"
    root_password: Is the Password of the root on Target Machine.
