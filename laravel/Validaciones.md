# Validaciones
## ¿Que es?

Como ya sabemos los usuarios nos intentearán *trolear* si no lo hacemos nosotros
primero al hacer las pruebas unitarias o en su defecto si no usemos herramientas
como pueden ser *phpUnit* , donde comprobará el código en la medida que nosotros
le señalemos.

Esto será nuestra primera linea de defensa contra la entrada de información,
no deseada.

## ¿Como comenzar?

Primero establecemos un formulario el cual mandamos para una una *action*
específica que nosotros queramos , en laravel `{{url('login')}}` no nos podemos
olvidar del **csrf** , que es cuanto menos importante en laravel.

## Archivo routes

Ahora una vez se nos envíe a la url de login , tenemos en *routes* , pero como
ya sabemos en esta versión la arquitectura de routes es la siguiente
`routes/web.php` que es donde nos guarda el contenido del router propiamente
dicho , ahora mismo tenemos un metodo que es el de acceso que es el `get` y otro
es el `post`.

La validación se hace en el `post` , aunque también se pueden realizar para no
tener más código del necesario en el controlador en el cual queremos introducir
la información luego en la base de datos.

## Ejemplo
* [Mis practicas en GitHub](https://github.com/jglantonio/learningLaravel/tree/learningValidations)
