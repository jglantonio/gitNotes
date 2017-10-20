# PHP
## 1 - Comandos
* `php -i` , es igual a hacer phpinfo();
* `php -v` , sirve para ver la versión de php.
* `php -l <file>` , comprueba si en el fichero hay un fallo de sintaxis.


## 2 - Funciones útiles
### 2.1 - Trabajo con strings
#### 2.1.1 - Contenido en un string `strpos`

Saber si una palabra se encuentra de un string específico.

```php
$valor = 'Hola desde mi github';
echo strpos($valor,'Hola'); // true
echo strpos($valor,'Adios'); // false
```
#### 2.1.2 - Logintud de un string `strlen`

```php
$valor = 'Hola';
echo strlen($valor); //4
```
#### 2.1.3 - Extrae un string de otro `substr`
Extrae  un string de otro , así solo extrayendo lo que se le señale.
substr($valor,<posicion>,<caracteres a coger>)

```php
$valor = 'Hola';
echo substr($valor,3,strlen($valor)); //a
echo substr($valor,0,1); //H
```

### 2.2 - Otras funciones

#### 2.2.1 - Número aleatorio `mt_rand`

Números aleatorios.

```php
$minimo = 1;
$maximo = 10;
mt_rand($minimo , $maximo);
```
* `mt_rand($minimo , $maximo);`
* `$minimo` valor minimo desde el que se ejecuta `mt_rand`
* `$maximo` valor máximo hasta el que se ejecuta `mt_rand`

## 3 - Otras cosas útiles
### 3.1 - Camuflar el link de una imagen.
Se redirige a un fichero html donde este tenga un header con una cabecera jpg o
de formato imagen , luego simplemente se pone el link original con la imagen
pasada por parámetro desde el php anterior.
