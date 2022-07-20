# Create Virtual Host in user dirctory

create user `sudo useradd -m exampleuser`

add existing user to www-data `usermod -a -G www-data example`

create folder *public_html* 

enable apache userdir `a2enmod userdir`

restart apache

add user to apache group `sudo usermod -a -G www-data exampleuser`

check it `grep ^www-data /etc/group`

enable mod rewrite `sudo a2enmod rewrite && sudo a2ensite example.conf`

`Require all granted` `AllowOverride None` `Allow from all` 
