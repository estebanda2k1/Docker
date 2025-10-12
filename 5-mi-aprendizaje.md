# COMANDOS DOCKER:

Descarga la imagen de una imagen

```
Docker pull
```

muestra las imágenes que se han creado en el contenedor.

```
Docker images
``` 

Obtener información detallada de un Docker en especifico.

```
Docker inspect
```

Eliminar una imagen del sistema Docker.

```
Docker rmi
```


Forzar la eliminación del sistema Docker, asi se este ejecutando.

```
Docker rmi -f
```


# CONTENEDORES:

Crear un contenedor:

```
Docker créate --name
```

 Listar todos los contenedores y las imágenes que tienen en uno
 
```
Docker ps -a
```

Iniciar un contenedor

```
Docker start <nombre>
```

ver los contenedores ejecutándose

```
Docker ps
``` 

Para crear un contenedor y ejecutarlo de manera inmediata.

```
docker run --name <nombre contenedor> <nombre imagen>:<tag>
``` 

Crear un contenedor pero ejecutarlo en SEGUNDO PLANO.

```
docker run -d --name <nombre contenedor> <nombre imagen>:tag
``` 

Eliminar un contenedor.

```
Docker rm
``` 

 Eliminar un contenedor que se esta ejecutando.
 
```
Docker rm -f
``` 

--Crear un mapeo de puertos (host y contenedor)--:

```
docker run -d --name <nombre contenedor> -p <puerto host>:<puerto contenedor> <nombre imagen>:<tag>
```
 
# *MAPEO  DE PUERTOS PARA CONTENEDORES*

Crear un mapeo de puertos, el comando -p permite esto:

```
docker run -d --name <nombre contenedor> -p <puerto host>:<puerto contenedor> <nombre imagen>:<tag>
```

Rastreo de mas de un puerto:

```
docker run -d --name <nombre contenedor> -p <puerto host 01>:<puerto contenedor 01> -p <puerto host 02>:<puerto contenedor 02> <nombre imagen>:<tag>
```

Forma semantica cuando se especifican puertos:

```
docker run -d --name <nombre contenedor> --publish published=<valorPuertoHost>,target=<valor> <nombre imagen>:<tag>
```

# *Operaciones en CONTENEDORES*

Ejecutar un comando dentro de un contenedor:

```
docker exec <nombre contenedor> <comando> <argumentos opcionales>
```

Shell interactivo: (comandos para consola despues de ejecutar el comando)

```
docker exec -i <nombre contenedor> /bin/bash 
```






