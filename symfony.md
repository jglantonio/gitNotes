# Symphony

Guia de instalación de symphony y notas.

## Instalacion
### Inicio
````
$ sudo mkdir -p /usr/local/bin
$ sudo curl -LsS https://symfony.com/installer -o /usr/local/bin/symfony
$ sudo chmod a+x /usr/local/bin/symfony
````
**Ejecutar la aplicacion**
````
cd aplicacion
php bin/console server:run
````
### Detalles

Todas las clases son creads en `app/` , las templates y configuraciones ne `src/`,
tenemos los cotroladores dentro de `src/AppBundle/controller` es donde están
los ficheros del controlador .

*Nota:* Si nos cargamos el controlador nos enocontraremos con un error **404**.

*Controlador* Las clases que construyen la página.

*Route* Dice que ruta hay que seguir para llegar a esa página
