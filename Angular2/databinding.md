# Databinding 

## html

* Hace referencia al guardar información en el módulo del formulario.
* Cuando ponemos entre `[]` un atributo de html , es una propiedad
* `(click)="<funcion()>"` un evento entre `()`.
* `*ngIf` , se espera una expresion si es cierto o falso , un if lógico.

Se usa una opción como un evento para cuando la carga es muy usual , pero si no 
se usa el `*ngIf` donde esto nos servirá para cargas más pesadas.

* Para el caso de Angular2 en diferencia del 1 , no tenemos problemas de que 
estemos pendientes del evento. No como en angular 1 que no para de estar pendientes
de los eventos.

* Con el atributo con nombre `ngModel` asignará el valor al que tenga asignado su
valor `ngModel="hola"` , asignará este valor direcamente.
* `[ngModel]` otra forma de definir una función en un evento.
* `[()]`Hace un doble binding. , apunta al input que está detnro del igual.

### ngOnInit()

En este sitio definiremos los inicios de las variables , es **mejor** que el propio
constructor que existe.