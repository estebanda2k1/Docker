# Imagen
### Descargar imagen
Descarga la última versión de la imagen disponible en el registro de Docker.

```
docker pull <nombre imagen> 
```

Descarga una versión específica de la imagen, cada imagen tiene etiquetas (tags) para diferentes versiones.
Una imagen puede tener la etiqueta latest para representar la última versión, si no se especifica una etiqueta se hará referencia a la versión latest.

```
docker pull <nombre imagen>:<tag>
```

<img width="957" height="171" alt="image" src="https://github.com/user-attachments/assets/6b978631-8e0f-4d3d-b568-96c51fdb13ff" />

El Sha-256 es el codigo de encriptacion que tiene el docker

Descargar la imagen **hello-world**
# COMPLETAR [x]


**¿Qué es nginx**

Es un software de código abierto que funciona como servidor web, reverse proxy (es un servidor intermediario que se ubica entre los clientes y uno o más servidores web para gestionar las solicitudes de red), balanceador de carga 

# COMPLETAR [x]

Descargar la imagen  **nginx** en la versión **alpine**

```
docker pull nginx:alpine
```

<img width="830" height="289" alt="image" src="https://github.com/user-attachments/assets/7fdbcafe-347c-41b2-a8e7-88b761ef2c87" />

# COMPLETAR [x]

### Listar imágenes

```
docker images
```
<img width="630" height="105" alt="image" src="https://github.com/user-attachments/assets/28785986-3f74-4f2e-8541-244d19d2a6ea" />


**Identificadores**

En Docker, se utilizan varios identificadores para diferenciar de manera única los elementos del sistema, como imágenes, contenedores, volúmenes y redes. Estos identificadores son generados automáticamente por Docker y son únicos dentro del contexto del sistema Docker en el que se encuentran. 

### Inspeccionar una imagen
El comando docker inspect se utiliza para obtener información detallada sobre un objeto de Docker específico, como un contenedor, una imagen, un volumen o una red.  Proporciona información en formato JSON sobre el objeto especificado.

```
docker inspect <nombre imagen>
docker inspect <nombre imagen>:<tag>
```

Inspeccionar la imagen hello-world 
# COMPLETAR [x]

**¿Con qué algoritmo se está generando el ID de la imagen**
Con el algoritmo SHA-256 


# COMPLETAR [x]

### Filtrar imágenes

```
docker images | grep <termino a buscar>

```

### Para eliminar una imagen
Eliminar permanentemente la imagen de tu sistema Docker.

```
docker rmi <nombre imagen>:<tag>
```

Eliminar la imagen hello-world 
Si se ejecuta el docker y se esta usando el container, salta este mensaje:

<img width="1099" height="75" alt="image" src="https://github.com/user-attachments/assets/0f6f8f2b-e455-4d1f-92c1-9e02fa1a88ba" />

# COMPLETAR [x]

Con el -f, ejecutandose el container:
<img width="539" height="63" alt="image" src="https://github.com/user-attachments/assets/2dc9a8cd-62bc-4bd7-bb68-76c7fdbba8cc" />


-f: Es la opción para forzar la eliminación de la imagen incluso si hay contenedores en ejecución que utilizan esa imagen.
Cuando eliminas una imagen Docker, Docker no elimina automáticamente los contenedores que se han creado a partir de esa imagen. Esto significa que, aunque hayas eliminado la imagen, el contenedor seguirá ejecutándose normalmente.  
**Considerar**
Eliminar una imagen no afecta a los contenedores que se han creado a partir de esa imagen, a menos que esos contenedores dependan de archivos o configuraciones específicas de la imagen eliminada. En ese caso, es posible que los contenedores se comporten de manera inesperada después de eliminar la imagen.
Es una buena práctica detener y eliminar todos los contenedores que dependan de una imagen antes de eliminar la imagen en sí.

```
docker rmi -f <nombre imagen>:<tag>
```
