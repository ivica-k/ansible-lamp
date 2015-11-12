# ansible-lamp

Installs LAMP stack with PHP 5.3 or 5.5

# Role variables

    mysql_config_path: '/etc/my.cnf'
	mysql_port: "3306"
	mysql_bind_address: '127.0.0.1'
	php_version: 5.5
	phpmyadmin_allowed_ip: 10.0.0.1

Example Playbook
----------------

    ---
	- hosts: my_server
	  sudo: yes
	  roles:
		 - php
		 - apache
		 - mysql
		 - phpmyadmin
		 
Run with
----------------
ansible-playbook -i hosts site.yml --extra-vars "mysql_root_password=INSERT_PASSWORD"