# PHP
## 1 - Comandos
* `php -i` , es igual a hacer phpinfo();
* `php -v` , sirve para ver la versión de php.
* `php -l <file>` , comprueba si en el fichero hay un fallo de sintaxis.


## 2 - Funciones útiles
### 2.1 - Trabajo con strings
#### 2.1.1 - Contenido en un string

Saber si una palabra se encuentra de un string específico.

```php
$valor = 'Hola desde mi github';
strpos($valor,'Hola'); // true
strpos($valor,'Adios'); // false
```

## 3 - Otras cosas útiles
### 3.1 - Camuflar el link de una imagen.
Se redirige a un fichero html donde este tenga un header con una cabecera jpg o
de formato imagen , luego simplemente se pone el link original con la imagen
pasada por parámetro desde el php anterior.
