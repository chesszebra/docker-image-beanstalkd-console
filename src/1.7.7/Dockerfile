FROM chesszebra/php:7.1-apache

# Change the work dir to the home directory
WORKDIR /root

# Install Composer
RUN curl -s http://getcomposer.org/installer | php

# Install the project
RUN php composer.phar create-project ptrofimov/beanstalk_console -s dev /var/www/html/ \
 && chown -R www-data:www-data /var/www/html

# Clean up
RUN rm composer.phar

# Change back the workdir
WORKDIR /var/www/html
