Comparando el conocimiento previo con el adquirido tras realizar la práctica, se detallan los aprendizajes principales y su impacto en la formación profesional. Además, se documenta la solución de cualquier problema encontrado durante la práctica.

---
**Imágenes y Contenedores:**

- **Imágenes de Docker**: Son plantillas de solo lectura que contienen las instrucciones necesarias para crear contenedores. Incluyen todas las bibliotecas y dependencias requeridas para ejecutar aplicaciones.

- **Contenedores de Docker**: Funcionan como entornos de ejecución ligeros y portátiles. Cada contenedor es una instancia de una imagen y contiene la aplicación junto con sus configuraciones específicas. Los contenedores son altamente portátiles y pueden ejecutarse en cualquier máquina con Docker instalado.

- **Creación de Imágenes**: Se utilizan archivos llamados Dockerfiles para especificar cómo construir una imagen. Estos archivos contienen instrucciones detalladas para configurar el entorno de ejecución.

- **Eliminación de Imágenes y Contenedores**: Se pueden eliminar imágenes y contenedores con comandos como `docker rmi` y `docker rm`, lo cual es esencial para gestionar el espacio de almacenamiento de manera eficiente.

**Mapeo de Puertos:**

El mapeo de puertos permite que los contenedores se comuniquen con el mundo exterior. Por ejemplo, se puede exponer un servicio web dentro de un contenedor en un puerto específico de la máquina host, lo cual es crucial para el desarrollo de aplicaciones web y servicios accesibles desde fuera del contenedor.

**Aplicación en Ingeniería:**


1. **Desarrollo Consistente**:
   Docker permite a los desarrolladores crear entornos de desarrollo que son idénticos a los de producción. Esto elimina el clásico problema de "funciona en mi máquina" al asegurar que el entorno de la aplicación sea consistente en todos los equipos.

2. **Despliegue Continuo**:
   Docker facilita la implementación continua (CI/CD) mediante la creación de imágenes de contenedores que pueden ser fácilmente desplegadas en cualquier entorno, ya sea de desarrollo, pruebas o producción. Las herramientas de CI/CD como Jenkins, GitLab CI, y CircleCI pueden integrarse con Docker para automatizar el proceso de construcción, prueba y despliegue.

3. **Microservicios**:
   Docker es fundamental en arquitecturas de microservicios. Permite que cada microservicio se ejecute en su propio contenedor, aislado del resto. Esto facilita la escalabilidad y el mantenimiento, ya que los servicios pueden actualizarse, escalearse o reiniciarse independientemente unos de otros.

4. **Pruebas y Control de Calidad**:
   Docker permite la creación de entornos de prueba aislados y replicables. Esto significa que los testers pueden ejecutar pruebas en entornos idénticos a los de producción, asegurando una mayor precisión en los resultados de las pruebas. Además, los entornos de prueba pueden destruirse y recrearse fácilmente, lo que es ideal para pruebas automatizadas.

5. **Simplificación de la Configuración**:
   Con Docker, la configuración de aplicaciones complejas puede definirse en archivos Dockerfile y docker-compose.yml. Esto permite que las configuraciones sean declarativas y fácilmente compartibles entre equipos. Nuevos desarrolladores pueden configurar su entorno de trabajo rápidamente usando estos archivos.

6. **Aislamiento de Entornos**:
   Docker proporciona aislamiento de procesos y recursos, lo que permite ejecutar múltiples aplicaciones o servicios en el mismo servidor sin conflictos. Esto es especialmente útil para ejecutar diferentes versiones de aplicaciones o para evitar conflictos de dependencia.

7. **Optimización de Recursos**:
   Los contenedores Docker son más ligeros que las máquinas virtuales tradicionales, lo que permite un uso más eficiente de los recursos del servidor. Esto es importante para escalar aplicaciones y optimizar los costos de infraestructura.

8. **Facilidad de Migración y Portabilidad**:
   Las aplicaciones empaquetadas en contenedores Docker pueden moverse fácilmente entre diferentes entornos, facilitando la migración y la portabilidad. Esto es particularmente útil para aplicaciones legacy que necesitan ser modernizadas y movidas a nuevos entornos de ejecución.

**Resolución de Problemas:**

Durante la práctica, no surgió ningún problema significativo.

En resumen, esta práctica mejoró significativamente la comprensión y las habilidades en el uso de Docker, aportando beneficios tangibles a la formación profesional en ingeniería de software.
