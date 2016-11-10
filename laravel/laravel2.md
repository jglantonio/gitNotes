# Laravel - 2 parte
## Ficheros.

### Route.php

Se usa lo siguiente :

`Route:get('<url>',<Acción a tomar>);`

 * Si hace referencia a `/`irá a `localhost/<miproyecto>/`

#### Notas

  1. Problema con Route cloud not find driver
  
Se soluciona descargando el : 

`sudo apt-get install php-mysql`

Luego nos dará un problema de permisos que tenemos que modificar en nuestro fichero `.env` , donde tenemos que poner los datos de la base de datos.
https://www.youtube.com/playlist?list=PLIcuwIrm4rKcFBd_YNNf70d6ai3HBlg3f
