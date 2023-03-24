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

## **Configuring nginx to use php processor**
- `sudo mkdir /var/www/projectLEMP`
- `sudo chown -R $USER:$USER /var/www/projectLEMP`
- `sudo nano /etc/nginx/sites-available/projectLEMP`
- `sudo ln -s /etc/nginx/sites-available/projectLEMP /etc/nginx/sites-enabled/`
![php-installation-success](./Images/successful-config-of-nginx.png)

### mysql successful login
`http://<Public-IP-Address>:80`

![nginx-site-test](./Images/nginx-projectlemp-test-on-web.png)

## **Testing php with nginx**
### creating info.php test file in root directory
`sudo nano /var/www/projectLEMP/info.php`

![info.php-site-test](./Images/php-test-with-nginx.png)

### removing info.php file from root directory
`sudo rm /var/www/projectLEMP/info.php`

![info.php-site-test](./Images/removing-Info.php-from-directory.png)

## **Accessing database content via PHP**
### test database creation
`CREATE DATABASE `test_database`;`

![creating_test_database](./Images/database-creation.png)
### test user creation with password
`CREATE USER 'example_user'@'%' IDENTIFIED WITH mysql_native_password BY 'password';`

![creating_user_and_password](./Images/user-creation.png)
### Granting new user Priviledges
`GRANT ALL ON example_database.* TO 'example_user'@'%';`

![Granting_priviledges](./Images/assigning-full-priviledge.png)
### new user Login
`mysql -u example_user -p`

![new_user_login](./Images/new-user-login.png)
### created database verification
`SHOW DATABASES;`

![database_verification](./Images/database-created.png)

### created database verification
`SHOW DATABASES;`

![database_verification](./Images/database-created.png)
### to_do list table creation
`CREATE TABLE test_database.todo_list ( item_id INT AUTO_INCREMENT, content VARCHAR(255), PRIMARY KEY(item_id) );`

![database_verification](./Images/todo_list-table-creation.png)
### populating to_do list table with values
`INSERT INTO test_database.todo_list (content) VALUES ("First item goes here");`

![populating_to-do_list](./Images/populating-database.png)
### accessing database content via php on web
`http://4.202.233.76/todo_list.php`

![accessing_database_content_via_php](./Images/database-content-access-via-web.png)