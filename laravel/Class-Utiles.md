# Class Auth

Es la clase que se encarga de lo relacionado con el login del usuario

## Funciones a tener en cuenta

* Esta función lo que hace es devolver toda la inforamción referente al usuario
 que se encuentra logeado en este momento `Auth::user()->{variable}`.
 Siendo `{variable}` los datos que contiene la base de datos , como idUser ,etc..
* La información de este está en `Users.php`.


# Class Guard

Manipula las sesiones , en este caso el `Auth::`
