#Laravel 4
## Middleware
Es el puente que podemos poner , que sería aconsejable entre el routing y la
view.
Es una forma de filtrado entre HTTP, el acceso de los usuarios a otras páginas
que no tengan porque acceder.
Al final el Middleware se encontrará dentro del routing , en los grupos de rutas,
dentro de los cuales crearemos los verbos correspondientes.

**Nota** Que los *verbos* son aquellos las palabras claves que están después de
`Route:<verbo>`.

## Crear nuestro Middleware

Tenemos que crearlo con el comando :</br>
`php artisan make:middleware <nombre>`<br>
Donde nosotros tendrémos la base del programa :

`````
<?php

namespace App\Http\Middleware;

use Closure;

class BeforeMiddleware
{
    public function handle($request, Closure $next)
    {
        // Perform action

        return $next($request);
    }
}
`````

Este también tenemos que definirlo en el kernel , en los distintos grupos que
existen.


https://laravel.com/docs/5.3/middleware
