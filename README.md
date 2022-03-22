## Ansible playbook for Nginx virtual host configuration
This ansible playbook set up nginx server with custom virtual host

## Preparation for launch

- Create Ubuntu server with Public IP
- Add you Host Name in Route 53
- Update variables ```hostname``` in nginx_install.yml with your Host Name
- Add your Public IP and User into inventory.txt file:
```
11.22.11.22 user=ubuntu
```
  If you need, you can add ssh key in inventory.txt file 
  ```ansible_ssh_private_key_file=/home/example/.ssh/aws.pem```

## Run playbook
```
ansible-playbook nginx_install.yml -i inventory.txt
```

## Inputs

- Your Host Name (nginx_install.yml)
- User Name (inventory.txt)
- Public IP (inventory.txt)