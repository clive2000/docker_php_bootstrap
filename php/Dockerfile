FROM php:7.2-fpm

RUN apt-get update \ 
	&& apt-get install -y \
        unzip

RUN docker-php-ext-install fileinfo \
	   && docker-php-ext-install opcache \
	   && docker-php-ext-install bcmath
		
COPY --from=composer:latest /usr/bin/composer /usr/local/bin/composer