# ATAJOS MYSQL
## Exportar base de datos

Exportar una base de datos entera

````
mysqldump -u <user> -p<password> nombreBaseDeDatos > baseDeDatos.sql
````
Exportar una tabla en concreto de una base de datos.
````
mysqldump -u <user> -p<password> nombreBasdeDatos tablaDeLaBaseDeDatos > NombreTablaAExportar.sql
````
## Para el error ERROR 1031 (HY000)

Este error se suele dar cuando se quiere importar.
````
sed -ie 's/ROW_FORMAT=FIXED//g' /<directorio>/baseDeDatos.sql 
sudo mysql -u user -p nombreBaseDeDatos < /<directorio>/baseDeDatos.sql 

````
## Matar una consulta en mysql
````
SHOW PROCESSLIST
KILL ID
````
## Exportar una consulta a un fichero csv

````
<Consulta_Select>
into outfile '<directorio>.csv' 
````
## Consultas

Sumatorio que esté especificado arriba en el select

ORDER BY <campo> WITH ROLLUP

## Comandos.
Mostrar todas las tablas :<br>
`show tables`<br>
Mostrar todas las tablas incluidas las vistas : 
`show full tables in <bd>`<br>

### Edición de tablas

Añadir una columna
````
ALTER TABLE <tabla> ADD <columna> DATETIME NOT NULL DEFAULT CURRENT_TIMESTAMP AFTER <columna>;
````
Eliminar una columna
````
ALTER TABLE <tabla> DROP <columna>;
````

NOTA : Para versiones mayores de 5.6.5 , para menores habría que meter en este campo el TIMESTAMP.
