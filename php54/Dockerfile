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
        php54 \
        php54-php-cli \
        php54-php-common \
        php54-php-dba \
        php54-php-devel \
        php54-php-embedded \
        php54-php-enchant \
        php54-php-fpm \
        php54-php-gd \
        php54-php-ldap \
        php54-php-mbstring \
        php54-php-mcrypt \
        php54-php-mssql \
        php54-php-odbc \
        php54-php-pecl-redis \
        php54-php-xml \
        php54-php-xmlrpc \
        openresty openresty-openssl openresty-pcre openresty-zlib

RUN ln -sv /usr/bin/php54 /usr/bin/php
RUN cd /tmp && curl --silent https://getcomposer.org/installer -o composer-install

