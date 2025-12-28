# my-aws-website

This project demonstrates the deployment of a responsive web environment on Amazon Web Services (AWS) using the Nginx web server on an Ubuntu Linux instance.

 Live Demo
Access the live deployment here:http://44.204.208.114/ (Note: Link may be inactive if the instance is currently stopped to manage costs.)

 Tech Stack & Infrastructure
Cloud Provider: AWS (Amazon Web Services)

Compute: EC2 Instance (t2.micro / Ubuntu 22.04 LTS)

Web Server: Nginx

Frontend: HTML5, CSS3

Terminal/SSH: Git Bash (Windows)

 Deployment Workflow
 
1. Instance Provisioning
Launched an Ubuntu instance within the AWS Free Tier.

Configured Security Groups to allow inbound traffic on:

Port 80 (HTTP): For public web access.

Port 22 (SSH): For secure remote management.

2. Server Configuration
Established a secure connection via SSH using RSA private keys (.pem).

Installed and initialized the Nginx service:

Bash

sudo apt update
sudo apt install nginx
sudo systemctl start nginx


3. File Deployment & Permissions
Transferred web assets to the server's web root at /var/www/html/.

Managed Linux file permissions to resolve 403 Forbidden errors:

Bash

sudo chown -R www-data:www-data /var/www/html
sudo chmod -R 755 /var/www/html
