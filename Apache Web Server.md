# Apache Web Server

#### Update and upgrade linux repo

`sudo apt update && upgrade -y`

#### Install Apache2 web server

`sudo apt install apache2`

then check apache2 status with `sudo systemctl status apache2`

#### Create Virtual Host

you can refer with this article [How To Set Up Apache Virtual Hosts on Ubuntu 18.04 | Linuxize](https://linuxize.com/post/how-to-set-up-apache-virtual-hosts-on-ubuntu-18-04/#:~:text=By%20default%20on%20Ubuntu%20systems,apache2%2Fsites%2Denabled%20directory.&text=ServerName%20%3A%20The%20domain%20that%20should%20match%20for%20this%20virtual%20host%20configuration.).

in this case we will put web in user directory, so we need to create user first.

1. `sudo adduser arif` 

2. check list all user `less /etc/passwd` or `cut -d: -f1 /etc/passwd`  or verify with `id arif`

3. add new user to sudo group with this command `sudo usermod -a -G sudo arif`

4. verify if new user successfully added to sudo `groups arif`

5. add existing user to Apache www-data group `sudo usermod -a -G www-data arif`

6. see list of member www-data group `grep ^www-data /etc/group`


