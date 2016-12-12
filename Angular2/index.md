# Index
## Introducción

Tenemos en el código fuente de la página el js , mientras que en el index.html
no aparece dicho js. Que es inyectado el webpack de forma dinámica a partir
del código fuente.

## Código

`app.component.ts`

`
import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
export class AppComponent {
  title = 'app works!';
}
`

`<nombre_variable> : <Tipo_variable> = <valor>`

