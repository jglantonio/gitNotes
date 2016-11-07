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
###  FUNCIONEN LAS DIRECCIONES CANONICAS
````
sudo nano /etc/apache2/sites-available/directorio.conf
<Directory /var/www/html/cestas>
    Options Indexes FollowSymLinks MultiViews
    AllowOverride All
    Order allow,deny
    allow from all
</Directory>
````
### Certificado ssl 

1. Se crea una carpeta ssl y dentro dos , una llamada crt y key

2. se ejecuta el comando para crear los certifados
````
openssl req -x509 -newkey rsa:4096 -keyout ./key/key.pem -out ./ctr/cert.pem -days 365 -subj '/CN=localhost'

http://stackoverflow.com/questions/10175812/how-to-create-a-self-signed-certificate-with-openssl
https://www.youtube.com/watch?v=X09cT8n2KeE
````
3. Habilitamos el uso del puerto implicados

**Notas** : Para saber si existen errores en la ejecutción .

````
journalctl -xe
````
