# ATAJOS MYSQL
## Exportar base de datos

````
mysqldump -u user -p nombreBaseDeDatos > baseDeDatos.sql

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
Mosntrar contenido de una tabla
`Show create view`<br>


