# ATAJOS MYSQL
## Exportar base de datos

Exportar una base de datos entera

```sql
mysqldump -u <user> -p<password> nombreBaseDeDatos > baseDeDatos.sql
```
Exportar una tabla en concreto de una base de datos.
```sql
mysqldump -u <user> -p<password> nombreBasdeDatos tablaDeLaBaseDeDatos > NombreTablaAExportar.sql
```
Importar una base de datos entera o una tabla de la base de datos.
```sql
mysql -u <user> -p namedb  < <table/db>.sql
```

## Para el error ERROR 1031 (HY000)

Este error se suele dar cuando se quiere importar.
```shell
sed -ie 's/ROW_FORMAT=FIXED//g' /<directorio>/baseDeDatos.sql 
sudo mysql -u user -p nombreBaseDeDatos < /<directorio>/baseDeDatos.sql 

```
## Matar una consulta en mysql
```sql
SHOW PROCESSLIST
KILL ID
```
## Exportar una consulta a un fichero csv

```sql
<Consulta_Select>
into outfile '<directorio>.csv' 
```
## Consultas

Sumatorio que esté especificado arriba en el select
```sql
ORDER BY <campo> WITH ROLLUP
```
### Edición de tablas
Copiar una tabla
```sql
CREATE TABLE <tabla_destino> SELECT * FROM <table_origen>;
```
Añadir una columna
```sql
ALTER TABLE <tabla> ADD <columna> DATETIME NOT NULL DEFAULT CURRENT_TIMESTAMP AFTER <columna>;
```
Editar columna
```sql
AlTER TABLE <tabla> MODIFY COLUMN NOT NULL <TYPE> DEFAULT <VALUE><NULL>;
```
Eliminar una columna
```sql
ALTER TABLE <tabla> DROP <columna>;
```
Reemplazar caracteres.
```sql
 UPDATE <table> SET <columna> = REPLACE(<columna>,<stringA>,<StringB>) WHERE value LIKE '%<StringA>%';
```
Renombrar una columna
```sql
RENAME TABLE <nombre_antiguo> TO <nuevo_nombre>
```
# NOTAS 
 * Para versiones mayores de 5.6.5 CURRENT_TIMESTAMP , pero para menores habría  que meter en este campo el TIMESTAMP.
