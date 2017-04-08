# Inicio
## Descripción

Es un CMS , un Content Manager System , que permite la administración y gestión de contenidos.

## Ficheros / carpetas de configuración.

* `wp-config.php`. Este fichero se encarga de la modificación de la base de datos , como de las claves de seguridad.

* `wp-content`. Almacena los ficheros que tratan sobre la customización de wordpress. plugins , etc ...
    * `index.php`. Este fichero hace referencia a `pagina.com/wp-contents`.
## Temas

Los temas tienen un fichero `index.php` que lo que tiene es todo el contenido de la página , porque realiza un bucle : 

```
	while ( have_posts() ) : the_post();
```

Donde recoge todosl os post que existen en la página.