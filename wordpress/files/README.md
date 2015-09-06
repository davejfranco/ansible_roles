#Ansible role - wordpress

This role provides a vanilla installation of wordpress, this role will download the latest version of wordpress
along with the installation of PHP5. Additionally there is wp-config.php as a template to provide custom
configuration according som variables to connect to mysql.  

###Variables
	user: "user of home directory" 
	domain: "domain of the wordpress server"
	db_name: "Mysql database name"
	db_user: "Mysql database username"
	db_password: "Mysql database password"
	
	

###Default values

	user: ""
	domain: "domain"
	db_name: "domain"
	db_user: "admin"
	db_password: "admin"

###Example
---

	- hosts: vagrant1
 	  sudo: yes

 	  vars:
 	   - user: vagrant
 	   - ssl: true
 	   - mode: "php_site"
 	   - db_name: "'user'"
 	   - db_user: "'user'"
 	   - db_password: "'password'"
 	   - domain: "domain"
 	   - host: "host"

	  roles:
	   - nginx
	   - wordpress


