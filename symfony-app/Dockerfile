FROM php:7.4-fpm

COPY get-composer /usr/local/bin/get-composer

RUN apt-get update && \
apt-get install -y --no-install-recommends \
git \
wget && \
wget https://get.symfony.com/cli/installer -O - | bash && \
ln -s /root/.symfony/bin/symfony /usr/local/bin/symfony
