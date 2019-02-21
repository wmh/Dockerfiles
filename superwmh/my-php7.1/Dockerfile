FROM 1and1internet/ubuntu-16-apache-php-7.1
LABEL maintainer="hunter.wu@gmail.com"

ENV DEBIAN_FRONTEND noninteractive

RUN apt update -y \
    && apt upgrade -y \
    && apt install -y php7.1-gmp php7.1-bc \
    && a2enmod rewrite \
    && sed -i 's/Listen 8080/Listen 80/' /etc/apache2/ports.conf \
    && sed -i 's/variables_order = "GPCS/variables_order = "EGPCS/' /etc/php/7.1/apache2/php.ini \
    && sed -i 's/variables_order = "GPCS/variables_order = "EGPCS/' /etc/php/7.1/cli/php.ini \
    && printf "\nIncludeOptional /data/conf/apache2/*.conf\n" >> /etc/apache2/apache2.conf
