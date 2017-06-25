# Docker

## Instalación

  1. Instalar Docker

## Tips&Trics
### Ver imágenes que están para instalar
Para encontrar las imágenes que nos interesa , podemos buscar con
`docker search <termino>`.

### Listar imagenes
Para listar las imágenes que tenemos instaladas , se ejecuta.
`docker images` , donde nosotros podemos ver la lista de elementos instalados.

`
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
ubuntu              latest              d355ed3537e9        4 days ago          119 MB
hello-world         latest              1815c82652c0        11 days ago         1.84 kB
`
### Ejecutar una imagen

`
sudo docker run -i -t <id> /bin/bash
`

