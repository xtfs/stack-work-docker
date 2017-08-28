FROM php:7.0.22-apache
RUN \
    apt-get update && \
    apt-get install libldap2-dev -y && \
    apt-get install libxml2-dev -y && \
    rm -rf /var/lib/apt/lists/* && \
    docker-php-ext-configure ldap --with-libdir=lib/x86_64-linux-gnu/ && \
    docker-php-ext-install ldap

RUN docker-php-ext-install pdo pdo_mysql
