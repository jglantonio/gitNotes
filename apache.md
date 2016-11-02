# APACHE
## TIPS

### Activar errores

Activar errores en apache , por salida en un fichero .log
```
nano /etc/php/apache2/php.ini`
```
En la linea se pone a `On`
```
log_errors = On`
```
Fuera de producción se pone a `Off`.

Log de errores como accesos están localizados en :
```
/var/log/apache2/
```
Tanto los errores como los accesos.

El sitio donde están localizados los ficheros de log se pueden ver en el directorio de :
```
less /var/log/apache2/envvars
```
## FUNCIONEN LAS DIRECCIONES CANONICAS
````
sudo nano /etc/apache2/sites-available/directorio.conf
<Directory /var/www/html/cestas>
    Options Indexes FollowSymLinks MultiViews
    AllowOverride All
    Order allow,deny
    allow from all
</Directory>
````
