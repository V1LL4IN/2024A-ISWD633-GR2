### Indicaciones para la práctica
El contenido solicitado entre paréntesis angulares debe ser reemplazado y los paréntesis angulares deben ser eliminados.

# Imagen
Es un archivo único que contiene todos los programas, librerías, dependencias y configuraciones necesarias para instalar y/o ejecutar una aplicación o un conjunto de aplicaciones.
![Imagen](imagenes/imagen.PNG)


## ¿Cuál es la relación entre una imagen y un contenedor? 
# COMPLETAR 

![Imagen y contenedores](imagenes/imagenYcontenedores.JPG)
## Comandos para imágenes

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
Una vez que iniciemos sesión, descargamos la siguiente imagen desde la terminal.

Descargar la imagen **hello-world**
```
docker pull hello-world
```
<img width="562" alt="image" src="https://github.com/V1LL4IN/2024A-ISWD633-GR2/assets/135792941/442c3d79-c414-4c01-ab23-d21ec3539c51">


**¿Qué es nginx**
Nginx es un servidor web de código abierto, de alto rendimiento, diseñado para servir tanto contenido estático como dinámico, así como para actuar como proxy inverso, equilibrador de carga, y proxy de correo. Fue desarrollado por Igor Sysoev y lanzado por primera vez en 2004. Nginx es un servidor web de código abierto, de alto rendimiento, diseñado para servir tanto contenido estático como dinámico, así como para actuar como proxy inverso, equilibrador de carga, y proxy de correo. Fue desarrollado por Igor Sysoev y lanzado por primera vez en 2004.

Descargar la imagen  **nginx** en la versión **alpine**
Desde la termina ejecutamos el comando
```
docker pull nginx:alpine
```
<img width="558" alt="image" src="https://github.com/V1LL4IN/2024A-ISWD633-GR2/assets/135792941/7e0a134a-fb00-4a94-81c4-a54f434a7f55">

### Listar imágenes

```
docker images
```
<img width="441" alt="image" src="https://github.com/V1LL4IN/2024A-ISWD633-GR2/assets/135792941/ad5b52df-5bba-4c90-b7f9-20992fa0b589">

**Identificadores**
En Docker, se utilizan varios identificadores para diferenciar de manera única los elementos del sistema, como imágenes, contenedores, volúmenes y redes. Estos identificadores son generados automáticamente por Docker y son únicos dentro del contexto del sistema Docker en el que se encuentran. 

### Inspeccionar una imagen
El comando docker inspect se utiliza para obtener información detallada sobre un objeto de Docker específico, como un contenedor, una imagen, un volumen o una red.  Proporciona información en formato JSON sobre el objeto especificado.

```
docker inspect <nombre imagen>
docker inspect <nombre imagen>:<tag>
```

Inspeccionar la imagen hello-world 

<img width="851" alt="image" src="https://github.com/V1LL4IN/2024A-ISWD633-GR2/assets/135792941/9bfb12b9-4b27-4f6e-b05b-cac6786968e2">


**¿Con qué algoritmo se está generando el ID de la imagen**
El ID de la imgaen se está generando con el algoritmo SHA256.
sha256:ee301c921b8aadc002973b2e0c3da17d701dcd994b606769a7e6eaa100b81d44

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
```
docker rmi hello-world:latest
```


-f: Es la opción para forzar la eliminación de la imagen incluso si hay contenedores en ejecución que utilizan esa imagen.
Cuando eliminas una imagen Docker, Docker no elimina automáticamente los contenedores que se han creado a partir de esa imagen. Esto significa que, aunque hayas eliminado la imagen, el contenedor seguirá ejecutándose normalmente.  
**Considerar**
Eliminar una imagen no afecta a los contenedores que se han creado a partir de esa imagen, a menos que esos contenedores dependan de archivos o configuraciones específicas de la imagen eliminada. En ese caso, es posible que los contenedores se comporten de manera inesperada después de eliminar la imagen.
Es una buena práctica detener y eliminar todos los contenedores que dependan de una imagen antes de eliminar la imagen en sí.

```
docker rmi -f <nombre imagen>:<tag>
```

