   BASE DE DATOS — SISTEMA DE TURNOS LIMAR
=============================================
Pasos para Crear y Desplegar la Base de Datos
---------------------------------------------

1.Iniciar el contenedor de PostgreSQL

Ejecuta el siguiente comando en la terminal para crear el contenedor que contendrá la base de datos:

 sudo docker run --name dbulimar -e POSTGRES_USER=ulimar -e POSTGRES_PASSWORD=ex4men_db -p 5432:5432 postgres:14

Este comando crea un contenedor llamado “dbulimar” con el usuario *ulimar* y la contraseña *ex4men_db*.

2.Desplegar pgAdmin4

sudo docker run --rm -p 5050:80 --link dbulimar:dbulimar -e "PGADMIN_DEFAULT_EMAIL=usuario@servilimar.com" -e "PGADMIN_DEFAULT_PASSWORD=limar#123" -d dpage/pgadmin4

3.Luego, abre tu navegador y entra a:

   http://localhost:5050

   **Credenciales de acceso:**
   - Usuario: usuario@servilimar.com
   - Contraseña: limar#123

4. Conectar pgAdmin con la base de datos

En pgAdmin, crea una nueva conexión con los siguientes datos:

   - **Nombre del servidor:** servilimar
   - **Host:** dirección IP del equipo
   - **Puerto:** 5432
   - **Usuario:** ulimar
   - **Contraseña:** ex4men_db

Una vez creada la conexión, podrás acceder y comenzar a crear tu esquema.

Autor
------
**Julian Meneses**  
Curso: Bases de Datos  
Año: 2025
