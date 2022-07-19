# Create Virtual Host in user dircetory

create user `sudo useradd -m exampleuser`

create folder *public_html* 

enable apache userdir `a2enmod userdir`

restart apache



add user to apache group `sudo usermod -a -G www-data exampleuser`

check it `grep ^www-data /etc/group`


