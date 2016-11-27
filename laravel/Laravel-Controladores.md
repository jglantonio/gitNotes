#Laravel5
## Controladores

En estos elementos que son los controladores se ejecuta la lógica del programa,
tal como en el middleware se ejecuta el control de accesso a la aplicación que
tenemos.

Controador es una clase usada para alogar ala lógica de enrutado.
ontiene metodos cono conocidos como acciones.

`php artisan make:controller <Nombre>Controller --resource`

esto nos crea un puñado de funciones :

* `index()` , donde redirigos al usuario
* `create()`  , este devuele un formulario y lo almacena en la base de datos de
  información recolectada , esto apuntaría a `nombrer.store`
* `store()` , como la palabra indica gestiona el formulario.

Entre otras muchas que se explican por si mismas.
