FROM phpdockerio/php56-fpm:latest
WORKDIR "/application"

# Fix debconf warnings upon build
ARG DEBIAN_FRONTEND=noninteractive

# Install selected extensions and other stuff
RUN apt-get update \
    && apt-get -y --no-install-recommends install  php5-memcached php5-mongo php5-mysql php5-pgsql php5-redis php5-sqlite php5-gd php5-gmp php5-gnupg php5-pecl-http php5-igbinary php5-imap php5-interbase php5-memcache php5-msgpack php5-oauth php5-radius php5-pspell php5-ssh2 php5-stomp php5-svn php5-twig php5-xmlrpc php5-xsl \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

# Install git
RUN apt-get update \
    && apt-get -y install git \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*