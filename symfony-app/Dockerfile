FROM php:7.4-fpm

ADD https://raw.githubusercontent.com/mlocati/docker-php-extension-installer/master/install-php-extensions /usr/local/bin/

COPY get-composer /usr/local/bin/get-composer

RUN cp $PHP_INI_DIR/php.ini-development $PHP_INI_DIR/php.ini && \
apt-get update && \
apt-get install -y --no-install-recommends \
git \
wget && \
wget https://get.symfony.com/cli/installer -O - | bash && \
ln -s /root/.symfony/bin/symfony /usr/local/bin/symfony && \
get-composer && \
mv composer.phar /usr/local/bin/composer
