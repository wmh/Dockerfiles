FROM ubuntu:14.04
LABEL maintainer="hunter.wu@gmail.com"

RUN apt update -y \
    && apt install -y apache2 php5 php5-apcu php5-curl php5-gd php5-gmp php5-mcrypt \
                      php5-memcache php5-memcached php5-mysql php5-sqlite \
                      php5-redis \
    && a2enmod rewrite \
    && printf "\n<Directory /data/app/>\n  Options Indexes FollowSymLinks\n  AllowOverride None\n  Require all granted\n</Directory>\n" >> /etc/apache2/apache2.conf \
    && echo 'ServerName 127.0.0.1' >> /etc/apache2/sites-available/000-default.conf

EXPOSE 80

CMD "/bin/bash"
