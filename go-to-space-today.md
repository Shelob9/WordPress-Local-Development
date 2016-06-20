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
