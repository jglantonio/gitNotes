# Artisan
## Comandos
Par crear un proyecto

`composer create-project --prefer-dist laravel/laravel`

Esto lo que hace es crear un proyecto en su última versión estable.

Ejecuta el servidor en el localhost:8000

`php artisan serve`

Para generar una cache de rutas que agilizan el trabajo

`php artisan route:cache`

Para limpiar la cache de rutas, sin que se generen nuevas :

`php artisan route:clear`

## Creación de elementos

El comando make te ayuda a crear distintos tipos de elementos :

Este primero te crea eñ controlador vacio.

`php artisan make:controller PhotoController`

este te crea el controlador con todas las clases que se suelen usar.

`php artisan make:controller PhotoController --resource`
