This project automates this github repository: https://github.com/kodekloudhub/learning-app-ecommerce

Requirements:
  In the same Network:
  1)Virtual Controller with Ansible installed (example: 192.168.56.75) (Ubuntu 20.04 used)
  2)Virtual Target (example: 192.168.56.101) (Ubuntu 20.04 used)
  
Configure the inventory file:
    Set the correct:
     1) ansible_host (Ip of the Target) 
     2) ansible_user  (User) 
     3) ansible_password (password to ssh to User)
     
Run the following command:
    ansible-playbook playbook.yml -i inventory.txt --extra-vars "ansible_sudo_pass={root_password}"
    root_password: Is the Password of the root on Target Machine.

Before running the playbook:
In the learning-app-commerce folder.
Create a file with name: 
  
  sudo vi .htaccess

Inside this paste the following:

        DirectoryIndex index.php
  

In the controller execute the following command:
    ansible-playbook playbook.yml -i inventory.txt --extra-vars "ansible_sudo_pass=target_root_password"
    
 To view the website visit from the browser:
 
    Target_Ip/learning-app-ecommerce/
    
    Example:
     
    http://192.168.56.101/learning-app-ecommerce/
    
