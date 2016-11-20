#Laravel 3
## Routing
Este fichero será el encargado de gestionar las urls que nosotros
definiremos en ellas como nos plazca.
Se definen con :
````
Route::get('my/page',function(){
    return 'Hello world';
});
````
Cabe destacar en el código que la construcción tiene su razón:
`Route::<verbo>(<url>,<accion>)`, como podemos ver tenemos un ¿verbo? si , es como se les llaman a las acciones después del route, estas acciones se llamrán así a partir de ahora , la segunda parte donde ponemos `accion` hace referencia a la lógica que se desarrollará a partir de ella.
Esto nos permitirá acceder a `localhost:8000/my/page`, con un mensaje de `Hello world` por ejemplo.

Podemos dividir estas acciones de forma más manejable , por ejemplo :
````
$logic = function(){
  return 'Hello World';
};
Route::get('my/page',$logic);
````
Para redirigir a un usuario que no ha iniciado sesión lo podemos redirigr de la siguiente manera.

````
Route::get('libros',function(){
    if(Auth::guest()){
        return Redirect::to('login');
    }
});
````
Los las urls como por ejemplo `<parte1>/<parte2>`.

````
Route::get('pez/{tipo?}',function($tipo){
    return "El pez es $tipo";
});
````
Para este caso , por ejemplo `$tipo` es la parte2 , y el parte1 es pez , 
por consiguiente la url que escribiríamos sería `localhost:8000/pez/gordo`esto accedería 
a dicha url , y nos pondŕia el texto "El pez gordo".

Para otros casos : 

````
Route::get('pez/{tipo?}',function($tipo){
    if ($genero == null){
        return "¿Opcion de pez?";
    }
    return "El pez es $tipo";
});
````
Esto redirige a otro sitio , es un if trivial.

### Metodos de routing.
* `Route::get()` , nos sirve como otro otro cualquiera
* `Route::post()` , también nos serviría pero este se usa por ejemplo para el caso de los formularios.
* `Route::match(['metodo1' , 'metodo2'],<Url>,<accción>)` , es un método que puede llamar a multiples verbos.
* `Route::any(<url>,<accion>)`, responde a cualquier verbo. 
* `Route::group(<middleware>=> <name>,<accion>){ actions de routing }`, responde a cualquier verbo , pero en un conjunto de verbos que puede estar dentro de lo que llamamos `actions de routing`. 
* `Route::controller(<direccion>,<controldor_nombre>)`, asocia una url a un controlador.
* `Route::make` , nos permite crear una nueva intancia de nuestro propio objeto.



## Notas
* Se aconseja usar los verbos correctos para una correcta programación y para que esta sea lo más transparente posible.
* Nos podemos fijar en el `tipo` que dicha variable tiene `?` eso quiere decir,  que dicha variable a poner es voluntaria,
el sacar eso de haí estamos diciendo que es obligatoria.

## Links

* http://laraveles.com/docs/5.0/controllers















