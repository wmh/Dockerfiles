FROM nimmis/apache-php7
LABEL maintainer="hunter.wu@gmail.com"

RUN apt update -y \
    && apt upgrade -y \
    && apt install -y php7.0-gmp \
    && a2enmod rewrite \
    && sed -i 's/variables_order = "GPCS/variables_order = "EGPCS/' /etc/php/7.0/apache2/php.ini \
    && sed -i 's/variables_order = "GPCS/variables_order = "EGPCS/' /etc/php/7.0/cli/php.ini \
    && sed -i 's/variables_order = "GPCS/variables_order = "EGPCS/' /etc/php/7.0/fpm/php.ini \
    && printf "\nIncludeOptional /data/conf/apache2/*.conf\n" >> /etc/apache2/apache2.conf
