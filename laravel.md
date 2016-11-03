# LARAVEL
## Empezar
### Instalar Composer

Primero hay que instalar el composer.

````
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('SHA384', 'composer-setup.php') === 'aa96f26c2b67226a324c27919f1eb05f21c248b987e6195cad9690d5c1ff713d53020a02ac8c217dbf90a7eacc9d141d') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"
````

Nos lo isntalará en :

````
~/.config/composer/vendor/laravel/installer
````
o como señala la página https://laravel.com/docs/4.2/quick en  : 
````
~/.composer/vendor/bin
````
### Instalar Laravel
composer global require "laravel/installer=~1.1"
Para inciar el proyecto
````
composer create-project laravel/laravel your-project-name 4.2.*
````
