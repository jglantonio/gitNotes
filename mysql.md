
#####Exportar base de datos

````
mysqldump -u user -p nombreBaseDeDatos > baseDeDatos.sql

````
##### Para el error ERROR 1031 (HY000)

Este error se suele dar cuando se quiere importar.
````
sed -ie 's/ROW_FORMAT=FIXED//g' /<directorio>/baseDeDatos.sql 

````
````
sudo mysql -u user -p nombreBaseDeDatos < /<directorio>/baseDeDatos.sql 

````