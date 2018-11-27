## **User Script (AWS)** 
### Title is a work in progress

```

# Bash Script in Progress for CentOS Flavored 'nix

# Just a standard bash script for the Amazon Linux AMI (as of 2018)

# She-bangs...Shebangs
#!/bin/bash

# updates current packages
yum update -y

# installs Apache 2.4, PHP 5.6 and Git (else it won't work!)
yum install httpd24 php56 git -y

# starts the Apache webserver so you can reach your instance on port 80
service httpd start

# reminds the server that it needs to ensure Apache starts up each time
chkconfig httpd on

# changes directory to the standard Apache index location
cd /var/www/html

# makes a one line php file for testing purposes 
echo "<?php phpinfo();?>" > test.php

```
