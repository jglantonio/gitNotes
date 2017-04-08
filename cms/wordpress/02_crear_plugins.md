# Los plugins

> Corred insensatos <br>
> by Gandalf *El gris*

## Introducción.

Enstan situados en la carpeta `wp-content` , dentro de la carpeta que ya pone `plugins`.

## Forma de crear un plugin

```
/ <Nombre del plugin>
    <Nombre del blugin>.php
    unistall.php
    /js
    /css
    /includes
    /images
```

### Comienzo del plugin

El comienzo de nuestro plugin tiene que ser : 

```
<?php
    /*
    Plugin Name:
    Plugin URI:
    Description:
    Author: 
    Author URI:
    License: 
    */
?>
```
Esto facilitará la forma en mostrarse al usuario al que realicemos el plugin en la descripción del mismo.
## Notas

* Siempre que quieras un plugin crealo desde cero.
* No modifiques plugins existentes para *"Mejorarlos"*, esp ten fe , cuando se actuaicen ocurrirá una desgracia.