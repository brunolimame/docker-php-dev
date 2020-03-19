FROM phpdockerio/php71-fpm:latest
WORKDIR "/application"

# Fix debconf warnings upon build
ARG DEBIAN_FRONTEND=noninteractive

# Install selected extensions and other stuff
RUN apt-get update \
    && apt-get -y --no-install-recommends install  php-memcached php7.1-mysql php7.1-pgsql php-redis php7.1-sqlite3 php7.1-bcmath php7.1-bz2 php7.1-dba php7.1-gd php7.1-gmp php7.1-imap php7.1-intl php-mongodb php-msgpack php7.1-odbc php7.1-phpdbg php7.1-pspell php7.1-soap php-ssh2 php7.1-xmlrpc php7.1-xsl php-yaml \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

# Install git
RUN apt-get update \
    && apt-get -y install git \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*