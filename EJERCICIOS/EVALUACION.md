## Práctica 1.

1. Introducción a base de datos

Objetivo: Identificar el nivel de comprensión de los conceptos de base de datos,
mediante preguntas abiertas.
 
Preguntas:

1. ¿Cuáles son las cinco funciones principales del administrador de bases de datos?
(valor 1.5)

Asegurar el buen funcionamiento de las bases de datos.
Retener los datos.
Proporcionarle seguridad a los datos que integran la BD.
Evitar la pérdida de la información de los datos.
Darle solución a las inconsistencias y/o pérdida de datos que se presenten en el sistema de base de datos.

2. Indíque cinco responsabilidades del sistema gestor de bases de datos (valor 1.5)

Instalar, configurar y gestionar las bases de datos.
Brindar soporte al equipo de desarrollo, la seguridad informática y redes.
Definir el esquema del diccionario de base de datos.
Especificar las restricciones de integridad para el aseguramiento de las bases de datos.
Garantizar la alta disponibilidad de las bases de datos.

3. En una BD al usuario del sistema se le brindarán recursos para realizar diversas
operaciones sobre estos archivos, tales como: (valor 1.5)

Creación de bases de datos, para integrar información de forma estructurada y así tener acceso a esos datos.
El usuario podrá mantener, editar o gestionar los datos, y la creación de informes de dichos datos.

4. ¿Qué es un Sistema de Información? (valor 1.5)

El Sistema de información permite la entrada, almacenamiento, procesamiento y salida de la información. Este sistema de información es un conjunto de elementos orientados al tratamiento y administración de los datos y la información generada.

## Práctica 2.

2. Diseño de un modelo relacional

Objetivo: Representar desde un modelo entidad relación un problema


Ejercicio:

Tenemos que diseñar una base de datos sobre proveedores y disponemos de la siguiente
información:

Realiza el modelo entidad relación. (valor 6)

Tenemos esta información sobre una cadena editorial:

● La editorial tiene varias sucursales, con su domicilio, teléfono y un código de
sucursal.

● Cada sucursal tiene varios empleados, de los cuales tendremos su nombre,
apellidos, NIF y teléfono. Un empleado trabaja en una única sucursal.

● En cada sucursal se publican varias revistas, de las que almacenaremos su título,
número de registro, periodicidad y tipo.

● Una revista puede ser publicada por varias sucursales.

● La editorial tiene periodistas (que no trabajan en las sucursales) que pueden
escribir artículos para varias revistas. Almacenaremos los mismos datos que para
los empleados, añadiendo su especialidad.

● También es necesario guardar las secciones fijas que tiene cada revista, que
constan de un título y una extensión.

● Para cada revista, almacenaremos información de cada ejemplar, que incluirá la
fecha, número de páginas y el número de ejemplares vendidos.
