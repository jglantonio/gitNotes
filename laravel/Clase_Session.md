# Clase Session
Clase de laravel , que viene a ser el `$_SESSION` de PHP , que tiene función propios para la gestión del contenido.
## Funciones 
Añadir una variable
```
Session::push(<key>,<value>)
```
Sacar una variabler.
```
Session::put(<key>)
```
Si existe la variable.
```
Session::exists(<key>)
```
Si variable se encuentra vacia
```
Session::has(<key>)
```
**Nota.-** Es distinto a que `exists` a `has`. Ya que puede llevar a una confusión la primera vez en cuanto a traducción
cuando la encuentran por primera vez.

## Link
 * [Clase de Session en la api de laravel](https://laravel.com/api/5.3/Illuminate/Http/Request.html)
