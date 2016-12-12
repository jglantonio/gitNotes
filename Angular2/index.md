# Index
## Introducción

Tenemos en el código fuente de la página el js , mientras que en el index.html
no aparece dicho js. Que es inyectado el webpack de forma dinámica a partir
del código fuente.

## Código

### `app.component.ts`

`import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
export class AppComponent {
  title = 'app works!';
}`

`<nombre_variable> : <Tipo_variable> = <valor>`

### `app.module.ts`

* Este sería el nombre estandar y de donde parte.
* Se importan modulos en `@NgModules`, que se establece una declaracion `declaration`,
 que es 'exporta' con `bootstrap`. 

### Notas

* La forma de comunicación entre los modulos son export e import , para pasarse las
variables.
* Se establece un módulo raíz por carpeta.
* Diferencias entre `let` y `var`, una variable que nos permite crear unas variables
por contexto , por ejemplo en los bucles `for`.
* `const` se considera una constante o lo que es lo mismo una variable final.
* Todos los nombres en minusculas y guiones medios y en typescript camelCase. 