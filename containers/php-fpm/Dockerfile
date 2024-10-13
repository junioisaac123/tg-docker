FROM  php:8.2-fpm-alpine

# Use the default production configuration
RUN mv "$PHP_INI_DIR/php.ini-development" "$PHP_INI_DIR/php.ini"

RUN apk add git curl libzip-dev libpng-dev libxml2-dev zip unzip bash oniguruma-dev vim neovim
RUN docker-php-ext-install pdo_mysql mbstring exif pcntl bcmath gd
RUN apk add npm
RUN /bin/bash -c "$(curl -fsSL https://php.new/install/linux)"
RUN echo 'export PATH="/root/.config/herd-lite/bin:\$PATH"' >> ~/.profile
RUN echo 'export PATH="/root/.config/herd-lite/bin:$PATH"' >> ~/.bashrc
# Instala Composer
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

# Establece el directorio de trabajo
WORKDIR /var/www/html

# Permisos
RUN chown -R www-data:www-data /var/www

# Exponer el puerto
EXPOSE 9000

# CMD ["php-fpm"]