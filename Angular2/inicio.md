# Angular 2 

## Inicio 

* Hay que instalar nodejs
* Hay que instalar angular js.

## Carpetas

* Las extensiones de ts , son de TypeScript

### class-flow
* karma.conf.js y protractor.conf.js , son ficheros de testing. 
### src
#### app
* `typings.d.ts` , nos permitirá dependinedo de las librerias
de terceros de los tipos , cosas que nos ayudará a lo largo de la programación
del proyecto , esto lo tocará el angular-cli
* `polyfills.ts` , permite el uso de js5 , pero que *'recomienda'* traer del 6 otras ,
pero también para compatibilidad con navegadores.
* `main.ts` , hace las importanciones necesarias para el programa , sería como una 
librería , es desde donde va tirando el *'webpack'* para ir tirando de la aplicación.


## Commandos

* `npm i`, carga el repositorio del json.
* `ng serve` crea un servidor https
* `npm i -g tslist` Es una herramienta de visual studio.

## Notas

* No se puede ejecutar `ng serve`mientras que no termine de descargar el paquete
de `npm i`.
* Los ficheros .map solo se generan para el modo dev.
* Para que se soporte Angular , hay que usar IE9 , ya que hay unos etiquetas
que no entenderá.