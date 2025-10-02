# Contenedores

### Crear un contenedor
Para crear un nuevo contenedor Docker a partir de una imagen específica, pero sin iniciarlo automáticamente. 

```
docker create --name <nombre contenedor> <nombre imagen>:<tag>
```
Crear el contenedor  **srv-web** usando la imagen nginx version alpine

<img width="618" height="63" alt="image" src="https://github.com/user-attachments/assets/01effe54-3975-447d-8a83-aa03e3ff4de3" />


# COMPLETAR [x]

Si creas un contenedor en Docker sin asignarle un nombre específico utilizando la opción --name, Docker asignará automáticamente un nombre aleatorio al contenedor. Este nombre suele consistir en una combinación de palabras y números.  

Crear el contenedor usando la imagen hello-world

Toca poner un argumento: 

<img width="598" height="99" alt="image" src="https://github.com/user-attachments/assets/7f846ae6-8765-4c4b-a9ad-119352c362e3" />


# COMPLETAR

### Listar los contenedores ejecutándose o no

```
docker ps -a
```

<img width="1312" height="119" alt="image" src="https://github.com/user-attachments/assets/9361b3f1-2070-426f-8c54-a827d68d4924" />


### Para iniciar un contenedor

```
docker start <nombre contenedor o identificador>
```
Iniciar el contenedor srv-web 

```
docker start srv-web
```

# COMPLETAR [x]

### Listar los contenedores ejecutándose
```
docker ps 
docker ps | grep <nombre contenedor>
```

### Para detener un contenedor

```
docker stop <nombre contenedor>
```

### Para crear un contenedor y ejecutarlo inmediatamente

```
docker run --name <nombre contenedor> <nombre imagen>:<tag>
```
![Ecosistema de Docker](dockerRun.PNG)

Crear y ejecutar inmediatamente el contenedor **srv-web2** usando la imagen nginx:alpine
# COMPLETAR [x]

```
docker run --name srv-web2 nginx:alpine
```

**¿Qué sucede luego de la ejecución del comando?**
Se puede observar el contenedor y como se ejecuta.

# COMPLETAR  [x]

Cuando ejecutas un contenedor en primer plano sin la opción -d (modo detach), el contenedor captura la entrada estándar (stdin) del terminal, lo que significa que el terminal queda "atrapado" y no puedes introducir más comandos hasta que detengas el contenedor.

### Para crear un contenedor y ejecutarlo inmediatamente sin estar vinculados al mismo (Ejecutar en segundo plano)
-d: Es la opción que indica a Docker que ejecute el contenedor en segundo plano (en modo "detach").
Cuando un contenedor se ejecuta en segundo plano, Docker devuelve el control al terminal inmediatamente después de iniciar el contenedor, lo que permite al usuario seguir ejecutando otros comandos en el mismo terminal sin que el contenedor detenga la interacción.

```
docker run -d --name <nombre contenedor> <nombre imagen>:tag
```
Crear y ejecutar inmediatamente el contenedor **srv-web3** en modo detach usando la imagen nginx:alpine

```
docker run -d --name srv-web3 nginx:alpine
``` 
# COMPLETAR [x]

### Para eliminar un contenedor

```
docker rm <nombre contenedor>
```
Eliminar el contenedor que se creó a partir de la imagen hello-world 
```
docker rm dreamy_swartz
```
# COMPLETAR [x]

Verificar que el contenedor que se eliminó 
```
docker ps -a
```
<img width="1164" height="139" alt="image" src="https://github.com/user-attachments/assets/9c477816-f760-45f9-af1a-8d65e1d44424" />


# COMPLETAR

### Para eliminar un contenedor que esté ejecutándose

```
docker rm -f <nombre contenedor>
```
Eliminar el contenedor **srv-web3** 

```
docker rm -f srv-web3
```

# COMPLETAR [x]

Verificar que el contenedor que se eliminó

```
docker ps -a
```

<img width="1185" height="176" alt="image" src="https://github.com/user-attachments/assets/26d1adcf-d6f3-4adf-9223-8db3a15b4865" />


# COMPLETAR [x]

### Para inspecionar un contenedor 

Inspeccionar el contenedor **srv-web** 
```
docker inspect srv-web
```
# COMPLETAR [x]
