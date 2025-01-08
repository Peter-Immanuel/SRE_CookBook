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


### Setup Certbot for SSL certificates
- sudo apt install certbot python3-certbot-nginx
- Create you server block under /etc/nginx/sites-available/_name_
- Create a symbolic link between site-availabe and site-enabled eg 
sudo ln -s /etc/nginx/sites-available/_example.com_ /etc/nginx/sites-enabled/
