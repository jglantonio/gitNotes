# LINUX
Comandos útiles en Linux
## 1. Comandos
### 1.1. Navegacion
Para navegar por las carpetas y saber algo en concreto se usa
` | grep "<expresion>"` para que solo tenga salida lo que queremos de dicho 
comando , por ejemplo , en una carpeta que tiene 3.232 elementos
y solo nos interesa el fichero que tenga el nombre "hola".
```
ls / -lR | grep "hola"
```
 * `l` para poner en detalle todos los documentos.
 * `R` que sea de forma recursiva
 * `|` pipe
 
### 1.2. Permisos
#### 1.2.1. Para carpetas
Para dar permisos a una carpeta 
```
sudo chmod 755 <carpeta>
```
Para dar permisos a las subcarpetas
```
sudo chmod 755 <carpeta> -R
```
#### 1.2.2. Para usuarios
Para asignar a un usuario de un grupo para el uso de una carpeta.
```
chown <propietario>:<grupo> <carpeta> 
```
## 1.3. Copiar ficheros
### 1.3.1. Copia normal
Para copiar normal : 

```
cp -r <origen>/<fichero> <destino>/>fichero>
```
### 1.3.2. Copia remoto
```
scp -r <user>@<ip>:/<dirección_fichero> <destino>
```
```
rsync -avzh <user>@<ip>:<directorio> <directorio destino> --recursive
```
### Busqueda

Para buscar una palabra en un fichero o directorio.
```
grep -r "texto" <directorio>
```
### 1.3.3 Datos de una carpeta
Contar los elementos que existen en una carpeta
````
ls | wc -l
```
Carpetas dentro de un directorio
```
ls -d */
```
