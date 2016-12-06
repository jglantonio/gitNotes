# Blade
## Introducción
* Toda pagina que quiera ser una blade , tiene que tener `<nombre>.blade.php`.

## Las `{{}}``
* En los blade todo lo que esté entre doble llaves se transforma en un echo.
* Con las dobles llaves , el código que no sea php , lo trunca a código ASCII.
* Para no escpar el contenido js hay que ponerlo `{{!! <code js> !!}}`.


## Inclusión de plantillas

** CORRERA SANGER CON ESTO **

* Se pueden usar `@Include()` , para añadir cabeceras o código html extra.
  * Solo hay que hacer referencia a la página que está situado en su mismo
  directorio y ya está.

## Herencia de html

Se pueden crear plantillas desde las cuales heredar el contenido y determinar en
los sitios que queremos que aparezca dicho contenido.

### `@Yield`
Esta etiqueta `@yield()` es un contenido por defecto que se mostrará.
### `@section` y `@show`
Son plantillas que se mostrarán siempre solo , si hay una plantilla hija que diga
lo contrario.
