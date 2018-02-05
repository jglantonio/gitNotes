# GIT
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
```
git-status
```
Creamos la nueva rama si no existen con “-b” hacemos que la cree. Sustituye a git branch <rama> y git checkout <rama>.
```
git checkout -b <rama>
```
Realizamos el commit para ver que ficheros han sido modificados
```
git commit
```
Añadimos los ficheros a los que realizar el commit. Para el caso de equivocarnos tenemos git reset , que señalamos el archivo que queremos eliminar de git add.
```
git add <fichero> o git add .
```
Realizamos el comentario de la actualización
```
git commit
```
Hacemos la subida dentro del origin a la rama que corresponde
```
git push origin <rama>
```
Descargamos dentro del origin a la rama que corresponde
```
git pull origin <rama>
```
Para eliminar los comentarios que tenemos de un commit
```
git reset
```

Para mezclar el contenido de dos ramas , tenemos la de origen que será a la 
que le queramos mezclar lo de un destino.
Por decirlo de otra manera el *"destino"* prebalece sobre el *"origen"*.
```
git merge <origen> <destino>
```

## TIPS
### Ir a un commit en concreto hacia atrás.
#### Paso 1
Hacer un reset hard a un punto en concreto del proyectos
```
git reset -- hard <id>
```
#### Paso 2
Luego si necesitamos hacer un push se realiza de la siguiente forma
```
git push origin <rama> --force
```
Con esto lo que hace será subir nuestro commit, pero eliminará todos
los que habia delante de este `id`en el `Paso 1`.

### Dejar de seguir un fichero o carpeta
Situacion : Dejar de seguir un fichero/carpeta que no queremos mantener
en nuestro repositorio git.

#### Para el caso de un directorio
```
 git rm --cached <directorio> -r
```
  * `-r` , haace el borrado de forma recursiva.
  
#### Para el caso de un fichero
```
 git rm --cached <fichero> 
```


### Eliminar una rama

Eliminar una rama creada por equivocación de forma local
```
git branch -D <rama>
```
`
git branch -D <rama>
`
Se puede dar el caso que queremos elimnar sobre el que estamos ,
la opción es cambiar a otra rama y desde esas ejecutar este comando.

## Clonar una rama en concreto

Para clonar una rama en concreto se hace :

`git clone -b <nombre_branch> <url_proyecto>`

## Acciones que hacer con una rama.
### Borrar de forma local una rama
```
git branch -D <nombre_branch>
```
```
git branch -d <nombre_branch>
```

### Modificar el nombre de una rama
```
git branch -m <nuevo_nombre>
```
o
```
git branch -m <viejo_nombre> <nuevo_nombre>
```
Con la primera consulta nos podemos ahorrar un `git bramch <rama>`

### Pasar de una rama a otra 
```
git branch -f <rama>
```
## Subir un directorio a un repositorio
```
cd <directorio>
git init
git add .
git commit -m 'mensaje'
git remote add origin <url>
git push push origin master
```
## Subir un directorio a una rama de nuestro repositorio
```
cd <directorio>
git init
git add .
git commit -m 'mensaje'
git remote add origin <url>
git checkout -b <rama>
git commit -m 'mensaje'
git push origin <rama>
```
## Crear un árbol en linea de comandos.
```
git log --graph --oneline --all
```
Tenemos la opcion `--decorate` para que salga más agradable a la vista. .
## Ver historial de git de los cambios locales realizados.
```
git log --all --pretty=format:"%h %cd %s (%an)" --since='20 days ago'
```
## Eliminar un repositorio remoto
```
git remote rm <nombre_repositorio>

```
Eso lo vemos con
```
git remote -v
```
Esto nos devolverá la infomración encesaria
## Cambiar el usuario en un commit 
Para cambiar el usuario en un commit , hay que ejecutar.
```
git commit --amend --author "New Author Name <New Author Email>"
```
## Links

* Repositorio de [GitHub .gitignores](https://github.com/github/gitignore).
* Formateo de texto en [este link](https://help.github.com/articles/basic-writing-and-formatting-syntax/)
* [githowto] (https://githowto.com/)
