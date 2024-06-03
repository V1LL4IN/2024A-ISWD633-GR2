# Contenedores

### Crear un contenedor
Para crear un nuevo contenedor Docker a partir de una imagen específica, pero sin iniciarlo automáticamente. 

```
docker create --name <nombre contenedor> <nombre imagen>:<tag>
```
Crear el contenedor  **srv-web** usando la imagen nginx version alpine
```
docker create --name srv-web nginx:alpine
```
<img width="603" alt="image" src="https://github.com/V1LL4IN/2024A-ISWD633-GR2/assets/135792941/b73a11aa-a5e7-48bb-aa2e-1ff274ba9902">


Si creas un contenedor en Docker sin asignarle un nombre específico utilizando la opción --name, Docker asignará automáticamente un nombre aleatorio al contenedor. Este nombre suele consistir en una combinación de palabras y números.  

Crear el contenedor usando la imagen hello-world
```
docker run --name contenedor-hello-world hello-world
```
<img width="682" alt="image" src="https://github.com/V1LL4IN/2024A-ISWD633-GR2/assets/135792941/70468bcd-b267-483f-87d7-5730d3921990">


### Listar los contenedores ejecutándose o no

```
docker ps -a
```

### Para iniciar un contenedor

```
docker start <nombre contenedor o identificador>
```
Iniciar el contenedor srv-web 

```
docker start srv-web
```
<img width="498" alt="image" src="https://github.com/V1LL4IN/2024A-ISWD633-GR2/assets/135792941/0182c6db-44ea-4ba2-85c5-42bb9ed94642">


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
![Ecosistema de Docker](imagenes/dockerRun.PNG)

Crear y ejecutar inmediatamente el contenedor **srv-web2** usando la imagen nginx:alpine
```
docker run --name srv-web2 nginx:alpine
```
<img width="693" alt="image" src="https://github.com/V1LL4IN/2024A-ISWD633-GR2/assets/135792941/608560a0-4bc2-45e4-9e96-5d8cb16c06dd">

**¿Qué sucede luego de la ejecución del comando?**

-Descarga de la Imagen:
Docker verifica si la imagen nginx:alpine está disponible localmente.
Si la imagen no está presente localmente, Docker la descarga del registro de Docker Hub o del registro configurado.

-Creación del Contenedor:
Docker crea un contenedor a partir de la imagen nginx:alpine.
Le asigna el nombre srv-web2 al contenedor. Este nombre es único y se utiliza para referirse al contenedor.

-Ejecución del Contenedor:
Docker inicia el contenedor ejecutando el comando principal especificado en la imagen nginx:alpine, que en este caso es el servidor Nginx.
El contenedor corre en primer plano (foreground) a menos que se especifiquen opciones adicionales para ejecutar en segundo plano (detached mode), como -d.

-Asignación de Recursos:
Docker asigna recursos del sistema (como CPU, memoria y redes) al contenedor.
Se establece un sistema de archivos específico para el contenedor, que incluye una capa de escritura sobre la imagen de solo lectura.

-Red y Puertos:
Docker configura una red para el contenedor. Por defecto, los contenedores usan la red bridge de Docker, a menos que se especifiquen otras opciones de red.
A menos que se especifique lo contrario, los puertos del contenedor no se exponen a la máquina host.

-Logs y Salida:
El contenedor comenzará a ejecutar Nginx y generará logs que se pueden ver usando comandos como docker logs srv-web2.


Cuando ejecutas un contenedor en primer plano sin la opción -d (modo detach), el contenedor captura la entrada estándar (stdin) del terminal, lo que significa que el terminal queda "atrapado" y no puedes introducir más comandos hasta que detengas el contenedor.

### Para crear un contenedor y ejecutarlo inmediatamente sin estar vinculados al mismo
-d: Es la opción que indica a Docker que ejecute el contenedor en segundo plano (en modo "detach").
Cuando un contenedor se ejecuta en segundo plano, Docker devuelve el control al terminal inmediatamente después de iniciar el contenedor, lo que permite al usuario seguir ejecutando otros comandos en el mismo terminal sin que el contenedor detenga la interacción.

```
docker run -d --name <nombre contenedor> <nombre imagen>:tag
```
Crear y ejecutar inmediatamente el contenedor **srv-web3** en modo detach usando la imagen nginx:alpine
```
docker run -d --name srv-web3 nginx:alpine
```
<img width="609" alt="image" src="https://github.com/V1LL4IN/2024A-ISWD633-GR2/assets/135792941/f3f30f4b-bdd2-47a2-81f6-ee61eb042703">


### Para eliminar un contenedor

```
docker rm <nombre contenedor>
```
Eliminar el contenedor que se creó a partir de la imagen hello-world 
```
docker rm mi-contenedor-hello-world
```
<img width="532" alt="image" src="https://github.com/V1LL4IN/2024A-ISWD633-GR2/assets/135792941/b5b9d152-7769-4718-bd5a-9c4c6d186cd8">



Verificar que el contenedor que se eliminó
```
docker ps -a
```
<img width="937" alt="image" src="https://github.com/V1LL4IN/2024A-ISWD633-GR2/assets/135792941/7b7526c5-1b88-458b-8cc0-1734e1fd3a6c">


### Para eliminar un contenedor que esté ejecutándose

```
docker rm -f <nombre contenedor>
```
Eliminar el contenedor **srv-web3** 

```
docker rm -f srv-web3
```

Verificar que el contenedor que se eliminó
```
docker ps -a
```
<img width="914" alt="image" src="https://github.com/V1LL4IN/2024A-ISWD633-GR2/assets/135792941/def5dada-07b2-4291-8b22-8d9409169bda">


### Para inspecionar un contenedor 

Inspeccionar el contenedor **srv-web** 
```
docker inspect srv-web
```
<img width="627" alt="image" src="https://github.com/V1LL4IN/2024A-ISWD633-GR2/assets/135792941/e2ad6a3a-c009-4a68-89bc-e586f55e6db8">

