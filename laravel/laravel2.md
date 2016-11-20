# Laravel - 2 parte
### Namespaces
Son una forma de establecer una dirección de un direcorio dentro del framework  
con esto eliminamos el hecho de instanciar los includes o requires.<br>
Nosotros podemos referencias con los namespaces de forma relativa. solo con un
slackspace , en Laravel ya sabe que nosotros nos referimos a una clase global del
framework `/perro` , de vez de definir `http/perro` , para instanciar la clase
en otro fichero.<br>
Existe otra forma de definir una clase , que por medio de los Namespaces sino
por medio de la keyworld `use` donde nosotros definimos la jerarquia que tiene
en el documento , como antes hicimos con `http/perro` , donde solo definimos el
namespace , por ejemplo tenemos también la palabra resevada como es `as`  donde
le nosotros le ponemos un *alias* a la clase. <br>
Estos namespaces tiene que ser definidos al inicio , antes de poner cualquier
código, porque sino no sería detectado y por que así lo establece el PSR-1

````
use http/perro;
$perro = new perro();
````
En otro caso tendríamos que hacer lo siguiente :
````
Namespaces http/perro;
$perro = new http/perro();
````
Con la definición de otra keyworld como es `as` nosotros renombramos el
namespaces que aparece en use , por ejemplo : <br>

````
use http/perro as chucho;
$perro = new chucho();
````
Aunque el `use` sea como el `import` de java , no podemos definir
un `import perro.*;` , sino tenemos que especificar todas las librerías a usar
o clases.

#### En resumen

Los namespaces se usan para establecer el nombre con el que se  le quiere hacer
referencia a esta clase , mientras que con el `use` , podemos definirla sin
necesidad de cuando la instanciemos tengamos que hacer todo el recorrido de
carpetas , simplemente usando el `use` , podemos definirla como si hubieramos
 hecho un `include`.


#### notas aclarativas.

* Nota 1 , estamos instanciando las clases en el fichero route.php que como
sabemos está en `app/http/route.php` , que a su vez es el redirector de nuestra
 aplicación web.

## Notas
<hr>
Problema con Route cloud not find driver
<hr>
````
sudo apt-get install php-mysql
````
Luego nos dará un problema de permisos que tenemos que modificar en nuestro
fichero `.env` , donde tenemos que poner los datos de la base de datos.
https://www.youtube.com/playlist?list=PLIcuwIrm4rKcFBd_YNNf70d6ai3HBlg3f
