# Restuarant website
To run this website on Liunx based systems (Centos, RHEL  etc) please follow the steps below.

#update yum packages

sudo yum -y update

#download httpd

sudo yum -y install httpd

#Install Git

sudo yum -y install git

#download code

git clone git@github.com:VirtualHost101/restaurant.git

# move source code (resturant's folder) to /var/www/httpd

sudo mv /resturant /var/www/httpd

#Change <documentroot> in /etc/httpd/conf/httpd.conf
  
sudo vi /etc/httpd/conf/httpd.conf

EDIT  DocumentRoot "/var/www/html      TO    DocumentRoot "/var/www/html/restaurant"


*** IMPORTANT*** MUST***  MAKE*** CHANGE** IN*** httpd.conf*** FILE**!!! 
  
# Check for Syntax errors 
  
httpd -t
  
** output should be (Syntax OK) **

#Start httpd service
  
sudo systemctl start httpd
  
{{ If the service is already started use " sudo systemctl restart httpd " }}

# Now you check your work in https://localhost:80 or https://ip-address:80

Thank You :)
