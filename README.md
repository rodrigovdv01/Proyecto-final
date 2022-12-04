# Proyecto-final

- Proyecto desarrollado para el curso de desarrollo basado en plataformas.

## Nombre del proyecto:

- Tu bici ideal

## Integrantes:
* Vásquez de Velasco Gonzales Vigil, Rodrigo - 202110682
* 


## Descripción del proyecto:

   * 
## Objetivos principales:

   *

## Mision:



## Vision:

# Application tools:

Vue
Vue CLI
Node
npm
Flask
Python

# Frameworks & Librerias:

## 1. Front-end
    *  Se utilizó Bootstrap 5, JavaScript, Vue.js y Vue Client

## 2. Backend
    * Flask
    * Flask - SQLAlchemy
    * Flask - Migrate 
    * Flask - WTF

## 3. Base de datos
    * PostgreSQL v14.2

## Script a ejecutar para iniciar el proyecto con datos:

En el 'models.py', al configurar el app, se colocó la DATABASE_URI con el path hacia la base de datos local.

# API's information. Request & Responces (endpoints):



## Hosts:

Se utilizaron un localhost diferente para el backend y frontend
   * Para el frontend, donde estaba Vue, se utilizó el puerto 8081.
   * Para el backend, donde corre Flask, se usó el 5000.

## Forma de auntenticación:

Recibe los datos ingresados al Login, hace una busqueda en la base de datos de Usuarios y si coinciden tanto Correo como Contraseña, redirige al inicio, donde manda los datos de dicho usuario.

## Error Handler:

Se crearon una respuesta formato JSON con los componentes: 'succes', 'code' y 'message'. 
Solo se crearon errorhandlers para los errares tipo 400, 403, 404, 422 y 500.

# Cómo ejecutar el sistema (Deployment scripts):

## Backend
   * export FLASK_APP=server
   * export FLASK_ENV=development
   * run flask

## Frontend
   * yarn serve
