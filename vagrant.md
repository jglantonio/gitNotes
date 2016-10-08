# VAGRANT FILE
## Introduccion
Herramienta de de ambientes virtuales de forma ligera.

## Instalación

Para instalar vagrant tenemos los siguientes caminos.

1. Instalamos por medio de linea de comandos.
````
sudo apt-get install vagrant
````
2. Lo descargamos de la página y lo Instalamos

## Empezar

1. Creamos el fichero del proyecto
2. Entramos en el fichero
3. Ejecutamos vagrant init para la creación del fichero `Vagrantfile`.
en el directorio raíz de nuestro fichero del punto 1. Ejeccutamos
el siguiente comando:
````
vagrant init
````
4. Creamos la maquina virtual en la que trabajaremos.
````
vagant box add <nombre_maquina> <link de descarga>
````
Para mi caso : http://files.vagrantup.com/precise32.box

5. Ponemos el nombre de nuestra maquina a la máquina en la linea
````
config.vm.box = "base"
````
a

````
config.vm.box = "<nombre_maquina>"
````

6. Ejecutamos en nuestro directorio `vagrant up`.
7. Ejecutamos el comando `vagrant ssh`.

## Notas

* Podemos modificar el fichero `/etc/hosts` , podemos poner la ip de nuestra
maquina y el nombre al que nos queramos referir.
`````
192.168.x.x <nombre_que_queramo>
`````
