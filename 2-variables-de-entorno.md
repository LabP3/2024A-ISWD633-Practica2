# Variables de Entorno
### ¿Qué son las variables de entorno
Son valores dinámicos que pueden afectar el comportamiento de un proceso en un sistema operativo. Estas variables se utilizan para almacenar información que puede ser necesaria para el funcionamiento de programas o scripts en un sistema.

### Para crear un contenedor con variables de entorno

```
docker run -d --name <nombre contenedor> -e <nombre variable1>=<valor1> -e <nombre variable2>=<valor2>
```

### Crear un contenedor a partir de la imagen de nginx:alpine con las siguientes variables de entorno: username y role. Para la variable de entorno rol asignar el valor admin.

![image](https://github.com/LabP3/2024A-ISWD633-Practica2/assets/171348095/ce20fd2b-65ad-4f41-872a-e09d7a92a629)

docker run -d --name nginx -e username=admin -e rol=admin nginx:alpine

### Crear un contenedor con mysql:8 , mapear todos los puertos

![image](https://github.com/LabP3/2024A-ISWD633-Practica2/assets/171348095/7fe181c8-b983-4af0-8dd3-aca1e450db58)

docker run -P -d --name mysql mysql:8

### ¿El contenedor se está ejecutando?

![image](https://github.com/LabP3/2024A-ISWD633-Practica2/assets/171348095/b7c3c34b-a0cd-483e-a03f-9106f59035f8)

NO

### Identificar el problema

Hay que especificar la contraseña del mysql.

### Eliminar el contenedor creado con mysql:8 

![image](https://github.com/LabP3/2024A-ISWD633-Practica2/assets/171348095/45ec2a20-5746-4841-9987-e498d50c9148)

### Para crear un contenedor con variables de entorno especificadas
- Portabilidad: Las aplicaciones se vuelven más portátiles y pueden ser desplegadas en diferentes entornos (desarrollo, pruebas, producción) simplemente cambiando el archivo de variables de entorno.
- Centralización: Todas las configuraciones importantes se centralizan en un solo lugar, lo que facilita la gestión y auditoría de las configuraciones.
- Consistencia: Asegura que todos los miembros del equipo de desarrollo o los entornos de despliegue utilicen las mismas configuraciones.
- Evitar Exposición en el Código: Mantener variables sensibles como contraseñas, claves API, y tokens fuera del código fuente reduce el riesgo de exposición accidental a través del control de versiones.
- Control de Acceso: Los archivos de variables de entorno pueden ser gestionados con permisos específicos, limitando quién puede ver o modificar la configuración sensible.

Previo a esto es necesario crear el archivo y colocar las variables en un archivo, **.env** se ha convertido en una convención estándar, pero también es posible usar cualquier extensión como **.txt**.
```
docker run -d --name <nombre contenedor> --env-file=<nombreArchivo>.<extensión> <nombre imagen>
```
**Considerar**
Es necesario especificar la ruta absoluta del archivo si este se encuentra en una ubicación diferente a la que estás ejecutando el comando docker run.

### Crear un contenedor con mysql:8 , mapear todos los puertos y configurar las variables de entorno mediante un archivo

![image](https://github.com/LabP3/2024A-ISWD633-Practica2/assets/171348095/638e1e05-2ae7-413a-8848-0c38b411769a)

![image](https://github.com/LabP3/2024A-ISWD633-Practica2/assets/171348095/cbb77862-8cdd-4e6d-a004-66a210dfa7c8)
 
### ¿Qué bases de datos existen en el contenedor creado?

![image](https://github.com/LabP3/2024A-ISWD633-Practica2/assets/171348095/09c8b3dd-2ebb-495f-9c41-74f2bb2e19bb)
