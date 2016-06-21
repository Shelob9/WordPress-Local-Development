#gdebi
https://apps.ubuntu.com/cat/applications/precise/gdebi/

# dependencies for phpStorm
sudo apt-get purge openjdk*

sudo add-apt-repository ppa:webupd8team/java

sudo apt-get update

sudo apt-get install oracle-java8-installer oracle-java8-set-default

# phpStorm -- version number changes
wget http://download-cf.jetbrains.com/webide/PhpStorm-2016.1.2.tar.gz

tar -xvf PhpStorm-2016.1.2.tar.gz

cd PhpStorm-145.1616.3/bin/

./phpstorm.sh

#atom
sudo add-apt-repository ppa:webupd8team/atom

sudo apt-get update

sudo apt-get install atom


#virtualbox
Download: http://download.virtualbox.org/virtualbox/5.0.22/virtualbox-5.0_5.0.22-108108~Ubuntu~xenial_amd64.deb

Installed with gedbi

#vagrant
Downlaod: https://releases.hashicorp.com/vagrant/1.8.4/vagrant_1.8.4_x86_64.deb

Install with gdebi

vagrant plugin install vagrant-vbguest

vagrant plugin install vagrant-ghost

vagrant plugin install vagrant-triggers

## MariaDB
[MariaDB](https://mariadb.org/) is an open-source, enhanced, drop-in replacement for MySQL.

Use the online [respository configuration tool](https://downloads.mariadb.org/mariadb/repositories) to generate installation instructions.

Sample install commands, based on Ubuntu Xenial, stable release, Irish mirror:

~~~
# Set up repo
sudo apt-get install software-properties-common
sudo apt-key adv --recv-keys --keyserver hkp://keyserver.ubuntu.com:80 0xF1656F24C74CD1D8
sudo add-apt-repository 'deb [arch=amd64,i386,ppc64el] http://ftp.heanet.ie/mirrors/mariadb/repo/10.1/ubuntu xenial main'

# Once the key is imported, install MariaDB:
sudo apt-get update
sudo apt-get install mariadb-server
~~~

Note that the URL for your repo is likely to differ depending upon your location.

You'll be prompted for a root password during the installation process.

After installation, secure MariaDB by removing anonymous users, removing the test database and disallowing external access. To achieve this, run:

~~~
sudo mysql_secure_installation
~~~

…and answer the questions accordingly.

## phpMyAdmin
[phpMyAdmin](https://www.phpmyadmin.net/) is a PHP tool that provides a web-based GUI for MySQL admin.

Install phpMyAdmin:

~~~
sudo apt-get install phpmyadmin apache2-utils
~~~

An [ncurses](https://en.wikipedia.org/wiki/Ncurses) window will open that enables phpMyAdmin to be configured.

* To select a server, hit space then tab/return
* Choose “yes” when asked “Configure database for phpmyadmin with dbconfig-common?”
* Enter a password for phpMyAdmin when prompted

Restart Apache:

~~~
sudo service apache2 restart
~~~

Access phpMyAdmin at [http://localhost/phpmyadmin](http://localhost/phpmyadmin).

Use the username 'root' and the password that you set during installation.

When installing phpMyAdmin on Xenial Xerus, you may encounter a white screen of death. Try checking the Apache error log to determine the problem:

~~~
tail -f /var/log/apache2/error.log
~~~

One reason for failure is a missing PHP extension. For example, phpMyAdmin requires the php-gettext extension. If necessary, install this and restart Apache:

~~~
sudo apt-get install php-gettext
sudo service apache2 restart
~~~

# SQL Manager

??

#php7

sudo apt-get install php7.0 php7.0-fpm php7.0-mysql -y

# git

sudo apt-get install git



# Composer
curl -s http://getcomposer.org/installer | php

sudo mv composer.phar /usr/local/bin/

# Set path variable for composer
??


# Node and NPM and Grunt CLI and Bower
curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash -

sudo apt-get install nodejs

sudo npm install -g grunt-cl

sudo npm install bower -g

# Create SSH key
ssh-keygen -t rsa -b 4096 -C "josh@joshpress.net"

Add it to Github/ Bitbucket

#Vagrant-based WP Dev
## Primary Vagrant
git clone --recursive https://github.com/ChrisWiegman/Primary-Vagrant.git PV

cd PV

vagrant up

## VVV
git clone https://github.com/Varying-Vagrant-Vagrants/VVV vvv

cd vvv

vagrant up

git clone https://github.com/bradp/vv.git

sudo cp vv /usr/local/bin


# Valet
## install php cURL if not already installed
sudo apt-get install curl

sudo apt-get install php-curl

## install Valet
composer global require cpriego/valet-ubuntu

## create valet dir
cd ~/

mkdir valet

cd valet

## run valet setup
valet install

valet park
