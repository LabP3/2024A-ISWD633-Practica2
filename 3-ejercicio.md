### Crear contenedor de Postgres sin que exponga los puertos. Usar la imagen: postgres:11.21-alpine3.17

![image](https://github.com/LabP3/2024A-ISWD633-Practica2/assets/171348095/5f1de0b0-a16e-46fa-b41e-dac143312fe4)

### Crear un cliente de postgres. Usar la imagen: dpage/pgadmin4

![image](https://github.com/LabP3/2024A-ISWD633-Practica2/assets/171348095/bb186f3d-7f1e-4bf1-82f7-f259a47721d3)

La figura presenta el esquema creado en donde los puertos son:
- a: (8080)
- b: (80)
- c: (5432)

![Imagen](imagenes/esquema-ejercicio3.PNG)

## Desde el cliente
### Acceder desde el cliente al servidor postgres creado.

![image](https://github.com/LabP3/2024A-ISWD633-Practica2/assets/171348095/8d443d6e-b9fd-4bd1-bcf5-33d30b97f907)

![image](https://github.com/LabP3/2024A-ISWD633-Practica2/assets/171348095/95c7d5e1-3f11-4ac2-9fec-8dc0b9dd876a)

### Crear la base de datos info, y dentro de esa base la tabla personas, con id (serial) y nombre (varchar), agregar un par de registros en la tabla, obligatorio incluir su nombre.

## Desde el servidor postgresl
### Acceder al servidor
### Conectarse a la base de datos info
### Realizar un select *from personas

![image](https://github.com/LabP3/2024A-ISWD633-Practica2/assets/171348095/9e84ed51-9874-49c9-a4a1-44bccefadde8)
