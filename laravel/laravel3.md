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

### Metodos de routing.
* `Route::get()` , nos sirve como otro otro cualquiera
* `Route::post()` , también nos serviría pero este se usa por ejemplo para el caso de los formularios.

## Notas
* Se aconseja usar los verbos correctos para una correcta programación y para que esta sea lo más transparente posible.
