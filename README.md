# Important Bash Command Line for Development of Web Application in Ubuntu

# LARAVEL-10.x
laravel 10.x setup on ubuntu 22.04.1

## Requirement
### 1. Update the package index
```bash
sudo apt-get update
```
### 2. Downloads and installs the most recent packages,
```bash
sudo apt-get upgrade
```
### 3. Install php 8 and extention required
```bash
sudo apt install php8.1-cli php-xml php-curl
```
### 4. Install composer
```bash
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('sha384', 'composer-setup.php') === 'e21205b207c3ff031906575712edab6f13eb0b361f2085f1f1237b7126d785e826a450292b6cfd1d64d92e6563bbde02') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"
sudo mv composer.phar /usr/local/bin/composer
composer -V
```
### 5. Install laravel global
```bash
composer global require laravel/installer
```
### 6. set up laravel bash
```bash
echo 'export PATH=~/.config/composer/vendor/bin:$PATH' >> ~/.bashrc
source ~/.bashrc
laravel -V
laravel new laravel-app
```
## VSCode Extention
1. Laravel blade snippets
2. PHP Namespace Resolver
3. PHP Intelephense

