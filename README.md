Getting started for Docker Engine CE (Free Version)
---------------------------------------------------

```
sudo mkdir -p build && cd build

sudo apt-get install git -y

sudo git clone https://github.com/drivesoft-technology/docker-awesome.git

cd docker-awesome
```


Install Docker Engine CE v18.06.1 (Free Version)
---------------------------------------------------

```
bash docker-install/install-docker-engine-on-ubuntu18.sh
```


Install Docker Compose v1.22.0
---------------------------------------------------

```
bash docker-install/install-docker-compose-on-ubuntu18.sh
```


Install PHP Composer
---------------------------------------------------

```
sudo apt-get install php7.2-cli -y
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('SHA384', 'composer-setup.php') === '93b54496392c062774670ac18b134c3b3a95e5a5e5c8f1a9f115f203b75bf9a129d5daa8ba6a13e2cc8a1da0806388a8') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php --filename=composer
mv composer /usr/local/bin/composer
php -r "unlink('composer-setup.php');"
```


Install LEMP (Linux-Nginx-MariaDB-Php7)
---------------------------------------------------

```
sudo git clone https://github.com/codestepz/phalcon3-app-template.git
```


Run Container | Phalcon Application Template
---------------------------------------------------

```
sudo docker-compose -f phalcon3-app-template/docker-compose.yml up -d
chmod 0777 -R phalcon3-app-template/www/runtime
```

```
http://[IP ADDRESS] << Phalcon. Nginx v1.15.4-alpine

http://[IP ADDRESS]/info.php << Demo. PHP v7.2.10 (FPM) 

http://[IP ADDRESS]:8080 << Demo. PhpMyAdmin v4.8.3
```