# Servidor para el PIN del Diplomado de Desarrollo FullStack

Para desarrollar el servidor del Proyecto Integrador se utilizó el lenguaje de programación PHP con su framework Laravel y una base de datos MySQL. 

## Las rutas
La aplicación cuenta con dos rutas principales:
* La ruta raíz (/): Que despliega la documentación del proyecto.
* La API post (/api/post): Que contiene la funcionalidad de validación de datos y registro.
Además. se agragó la api de testing `answer`, que sirve para verificar la conección con el cliente.

## Las vistas
Para completar el proyecto se desarrollaron dos vistas:
* answer: Una vista que devuelve la respuesta a todas las preguntas.
* mail: la vista con la plantilla para el correo de verificación.

## El diseño
Para diseñar la aplicación se utilizó el patrón MVC (_Modelo Vista Controlador_). Con esto en mente se comenzó el proyecto diseñando la base de datos, creando la migración de la tabla `contacts`correspondiente con el registro de contactos.  
Luego, a partir de esta migración, se creó el modelo `avisoContacto.php` y luego, en `ContactController.php`, se programó la lógica de validación y almacenamiento de datos.  
Por último, se conectó el controlador a la  API `post` en el archivo `api.php`.

## El funcionamiento
El funcionamientio del programa es simple y podría explicarse en el siguiente orden:
* La API `post` recibe una solicitud y pasa la información al ContactController.

