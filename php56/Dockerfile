FROM centos:7

# ENV LANG=en_US.UTF-8
# ENV LC_ALL=en_US.UTF-8
# ENV LC_COLLATE=C

RUN groupadd --system www
RUN useradd --system --home-dir /var/www -g www --shell /sbin/nologin www

RUN yum update -y
RUN yum install -y curl wget bsdtar3 htop yum-utils
RUN yum install -y https://cdn.centos.no/remi/enterprise/remi-release-7.rpm
RUN curl --silent https://openresty.org/package/centos/openresty.repo -o /etc/yum.repos.d/openresty.repo

RUN yum install -y \
        php56 \
        php56-php-cli \
        php56-php-common \
        php56-php-dba \
        php56-php-devel \
        php56-php-embedded \
        php56-php-enchant \
        php56-php-fpm \
        php56-php-gd \
        php56-php-ldap \
        php56-php-mbstring \
        php56-php-mcrypt \
        php56-php-mssql \
        php56-php-odbc \
        php56-php-pecl-redis \
        php56-php-xml \
        php56-php-xmlrpc \
        openresty openresty-openssl openresty-pcre openresty-zlib

RUN ln -sv /usr/bin/php56 /usr/bin/php
RUN cd /tmp && curl --silent https://getcomposer.org/installer -o composer-install

