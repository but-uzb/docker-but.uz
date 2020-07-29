FROM php:7.4-fpm

COPY --from=composer:2.0.0-alpha2 /usr/bin/composer /usr/bin/composer

COPY --from=mlocati/php-extension-installer /usr/bin/install-php-extensions /usr/bin/

RUN install-php-extensions bcmath zip intl gettext gd pdo_mysql mysqli

RUN mv "$PHP_INI_DIR/php.ini-development" "$PHP_INI_DIR/php.ini"
