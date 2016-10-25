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
