FROM debian:jessie

ENV SYMFONY_HOME /var/www/symfony

RUN apt-get update && apt-get install -y curl php5-cli
RUN curl -LsS http://symfony.com/installer -o /usr/local/bin/symfony
RUN chmod a+x /usr/local/bin/symfony

RUN mkdir -p "$SYMFONY_HOME"

RUN useradd -d "$SYMFONY_HOME" -u 1000 -g www-data -s /bin/bash symfony
RUN chown -R symfony:www-data "$SYMFONY_HOME"

USER symfony
