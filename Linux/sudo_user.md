# Ubuntu Server Setup for Backend Development


### Setup User with sudo privileges
- ssh root@__vm_ip_address__
- Cmd: adduser _username_
- Cmd: usermod -aG sudo _username_
- Test command su - _username_

### Install Docker 
- [Setup Docker](https://docs.docker.com/engine/install/ubuntu/)

### Post Docker Setup, user docker with sudo 

- sudo groupadd docker
- sudo usermod -aG docker $USER
- newgrp docker
- Test command

### Install Nginx 
- sudo apt update
- sudo apt install nginx
- sudo ufw app list
- sudo ufw allow 'Nginx Full'

#### Manage Nginx 
- sudo systemctl (start | stop | status | restart) nginx






