## **Documentation for Project 2**

### nginx Installation 

`sudo apt update`
`sudo apt install nginx`

`sudo systemctl status nginx`

### nginx Server Installation Process
![nginx-server-Installation-process](./Images/nginx-installation-process.png)

![nginx-server-Installation-success](./Images/nginx-successful-installation.png)

### Opening nginx port 80
`curl http://localhost:80`

![nginx-port80-opening](./Images/nginx-port80-opening.png)

### nginx server internet response test
`http://<Public-IP-Address>:80`

![nginx-Internet-test](./Images/nginx-port80-activation.png)

## **Mysql Installation**
- `sudo apt install mysql-server`
- `sudo mysql`

![sql-server-installation-success](./Images/mysql-connection-success.png)

### mysql security script 
`sudo mysql_secure_installation`
`ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'PassWord.1';`

![sql-server-security-script](./Images/security-script.png)

### mysql successful login
`sudo mysql -p`

![sql-server-login-success](./Images/mysql-login-success.png)

## **PHP Installation**
`sudo apt install php-fpm php-mysql`
![php-installation-success](./Images/php-Installation-success.png)