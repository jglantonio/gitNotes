# LINUX
Comandos útiles en Linux
## 1. Comandos
### 1.1. Navegacion
Para navegar por las carpetas y saber algo en concreto se usa
`more` para que solgo tenga salida lo que queremos de dicho 
comando , por ejemplo , en una carpeta que tiene 3.232 elementos
y solo nos interesa el fichero que tenga el nombre "hola".
```
ls / -lR | grep "hola"
```
 * `l` para poner en detalle todos los documentos.
 * `R` que sea de forma recursiva
 
### 1.2. Permisos
#### 1.2.1. Para carpetas
Para dar permisos a una carpeta 
```
sudo chmod 777 <carpeta>
```
Para dar permisos a las subcarpetas
```
sudo chmod 777 <carpeta> -R
```
#### 1.2.2. Para usuarios
Para dar permisos a los usuarios
```
chown <propietario>:<grupo> <carpeta> 
```
