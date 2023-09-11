# WordPress-Demo
## The following step by step process provides with the setup of WordPress application on AWS Cloud, provisioing servers, assinging IP Addresses and perform work flow actions:
* To create a sample website on AWS Cloud, we need to launch AWS ubuntu 22.04 version instance.
* We have to assign the domain for the IP.
* Set up the CI/CD with github actions in .github file 
* Install nginx using the following command:
     ##### apt install nginx
* Install MySQL using the following command:
     ##### apt install mysql-server
* Create Alter Root User for MySQL Shell using the following command:
     ##### ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password by 'root@123';
* Create DataBse User:  
     ##### CREATE USER 'ejaz'@localhost IDENTIFIED BY 'fareejaz@123';
* Create DataBase:
     ##### CREATE DATABASE wordpress;
* Grant all privileges to the user created:
     ##### GRANT ALL PRIVILEGES ON wordpress.* TO 'ejaz'@localhost;
* Install required PHP Packages:
     ##### sudo apt update
     ##### sudo apt install php-fpm
     ##### sudo systemctl start php8.1-fpm   # Use the appropriate PHP version
     ##### sudo systemctl enable php8.1-fpm  # Use the appropriate PHP version
* Clone the code from the below site: 
     ##### git clone https://github.com/ejazali1510/wordpress-demo.git
* Create the configuration files:
     ##### cd /etc/nginx/sites-enabled
* Restart the nginx service:
     ##### systemctl restart nginx
