FROM php:7.4-fpm-alpine

RUN if [ $WITH_XDEBUG = "true" ] ; then \
        pecl install xdebug; \
        echo "error_reporting = E_ALL" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini; \
        echo "display_startup_errors = On" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini; \
        echo "display_errors = On" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini; \
        echo "xdebug.idekey=$XDEBUG_IDEKEY\n" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini \
        echo "xdebug.remote_enable=1" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini; \
        echo "xdebug.remote_hort=$REMOTE_HOST\n" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini \
        echo "xdebug.remote_port=$REMOTE_POST\n" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini \
        docker-php-ext-enable xdebug; \
    fi ;
