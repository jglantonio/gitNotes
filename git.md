#GIT
## Comandos

- git log -x , x  es los commits que hay hacia atrás
- git status , donde está el git
- git fetch
- git pull , descarga de ficheros
- git push , upload de ficheros
- git chechout -b <> , crea un branch
- git diff , para ver las diferencias en el código
- git commit ,
- git reset <fichero> , elimina un git add de un fichero en concreto.

##Primeros pasos

Primero sabemos donde estamos
````
git-status
````
Creamos la nueva rama si no existen con “-b” hacemos que la cree. Sustituye a git branch <rama> y git checkout <rama>.
````
git checkout -b <rama>
````
Realizamos el commit para ver que ficheros han sido modificados
````
git commit
````
Añadimos los ficheros a los que realizar el commit. Para el caso de equivocarnos tenemos git reset , que señalamos el archivo que queremos eliminar de git add.
````
git add <fichero> o git add .
````
Realizamos el comentario de la actualización
````
git commit
````
Hacemos la subida dentro del origin a la rama que corresponde
````
git push origin <rama>
````
Descargamos dentro del origin a la rama que corresponde
````
git pull origin <rama>
````
Hacer un reset hard a un punto en concreto del proyectos
````
git reset -- hard <id>
````
Eliminar una rama creada por equivocación de forma local
````
git branch -D <rama>
````
