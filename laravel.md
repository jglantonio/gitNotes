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
### Instalar Servidor con Laravel
composer global require "laravel/installer=~1.1"
Para inciar el proyecto
````
composer create-project laravel/laravel your-project-name 4.2.*
o
composer	create-project	laravel/laravel	miweb	--prefer-dist
````
*Nota :* Es necesario el phpXX-mcrypt 

Damos todos los permisos a las carpetas storage y bootstrap/cache
se ejecuta el servidor de laravel : 
````
php artisan serve --port=8080
````
En caso de tener otro tipo de hosting local no hace falta acceder , como en el caso de tener instalado Apache , X/L/Wampp en su defecto , es como en php que también puede ejecutar su propio servidor.

### Carpetas y ficheros
#### Carpetas
* app , codigo de la aplicaicón.
* config , configuración de la aplicación.
* databsae , definición de la base de datos. 
* public , se aloja el contenido público y los archivos css , js y otros de dominio público.
* resources , tiene otras carpetas : 
  * view , plantillas HTML , que usean los controladores , pero no se almacena el s ni css o imágenes , que se ala macenan el a carpeta de `public`
  * lang , Se guardan los arhivos php , donde están los arrays de los distintos idiomas.
  * assets , fuentes del tipo less o sass , no se suele usar porque se escribe directamente en `public`
* bootstrap , 
* storage , información necesaria para la ejecución de la web.
* test , pruebas de PHPUnit.
* vendor , librerias y dependencias del framework de Laravel,  que se actualiza por lo instalado anteriormente que es composer.

#### Ficheros

https://www.gitbook.com/book/ajgallego/laravel-5/details

## Notas
* En el fichero `config`tenemos la configuración de nuestro proyecto
* Fichero `.env` para las variables de entorno
* Para saber la versión de laravel instalada es en el directorio local `php artisan --version`
