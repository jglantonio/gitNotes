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
 * http/Controllers , Contiene los contralores que interactuarán con los modelos.
 * http/Middleware , validación de permisos y clases intermedias.
 * http/route.php , es el fichero que define las rutas de nuestros direcotiros.
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

* `.env` , este fichero ya se dijo que contiene la configuración del host en el que se encuentra y tiene que estar excluido de nuestro fichero `.gitignore` , para que no lo suba y la configuración sea independiente entre equipos y no machaque la configuración de las peronas que estén trabajando en nuestro proyecto.
* composer.json , contiene las dependencias instaladas por laravel. Se puede introducir a mano para librerías externas no incluidas en las librerías de laravel.

https://www.gitbook.com/book/ajgallego/laravel-5/details
http://www.desarrolloweb.com/articulos/tareas-instalacion-laravel5-problemas.html

### php	artisan
Para saber las rutas que tenemos en nuestro fichero route.php
````
php artisan route:list
````

````
php artisan 
````
Para ejecutar nuestro servidor web en el puerto 8080
````
php artisan serve --port=8080
````
## Notas
* En el fichero `config`tenemos la configuración de nuestro proyecto
* Fichero `.env` para las variables de entorno
* Para saber la versión de laravel instalada es en el directorio local `php artisan --version`

