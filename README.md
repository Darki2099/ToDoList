Este proyecto es una API de gestión de tareas desarrollada con Node.js, Express y SQLite. Permite a los usuarios registrarse, iniciar sesión, crear, actualizar, eliminar y completar tareas. 
El propósito del proyecto es proporcionar un sistema sencillo y seguro para la gestión de tareas personales, con un enfoque en la autenticación de usuarios mediante JWT (JSON Web Token).

Para clonar este repositorio e instalar todas las dependencias necesarias:
Clona el repositorio:
git clone https://github.com/tu-usuario/tu-repositorio.git

Navega al directorio del proyecto:
cd tu-repositorio

Instala las dependencias:
npm install init -y
npm install express sqlite3 body-parser
npm install express 
npm install ws

Instrucciones para ejecutar el programa:
Tras llegar al directorio ejecutar con el comando: node servidorp.js
El servidor se ejecutará en http://localhost:3000.

Autenticación
POST /register: Registro de un nuevo usuario.
POST /login: Inicio de sesión y obtención de un token JWT.
POST /logout: Cerrar sesión y revocar el token.

Gestión de Tareas (CRUD)
POST /tareas: Crear una nueva tarea (requiere autenticación).
GET /tareas: Obtener todas las tareas pendientes del usuario autenticado.
PUT /tareas/:id: Actualizar una tarea específica (requiere autenticación).
DELETE /tareas/:id: Eliminar una tarea específica (requiere autenticación).
POST /tareas/completar/:id: Marcar una tarea como completada (requiere autenticación).
GET /tareas/completadas: Obtener todas las tareas completadas del usuario autenticado.
DELETE /completadas/:id: Eliminar una tarea completada (requiere autenticación).

Tecnologías Utilizadas
Este proyecto utiliza las siguientes tecnologías:

Node.js: Plataforma de desarrollo en JavaScript para el backend.
Express: Framework minimalista para la creación de aplicaciones web y APIs.
SQLite: Base de datos ligera utilizada para almacenar la información de usuarios y tareas.
Sequelize: ORM (Object-Relational Mapping) para manejar la base de datos SQLite.
JWT (JSON Web Token): Para la autenticación segura de usuarios.
bcrypt: Biblioteca para el hashing seguro de contraseñas.
