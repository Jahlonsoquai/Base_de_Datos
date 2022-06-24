## Práctica 3.
### Introducción a SQL
Objetivo: Demostrar la correcta identificación de los conceptos del lenguaje SQL
Ejercicio:

1. Menciona los comandos DMl: (valor .85)

    Los comandos DML permiten consultar, filtrar y extraer datos de la base de datos y así organizarlos.
    SELECT. Para realizar consultas de registros en la base de datos, que satisfagan un criterio determinado.
    UPDATE. Para realizar modificaciones en los valores de los campos y en los registros especificados.
    INSERT. Para cargar lotes de datos en una única operación. 
    DELETE. Para eliminar registros de las tablas.

2. Menciona 3 tipos de datos que existen: (valor .85)

    Carácteres y cádenas de carácteres, Flotantes o de punto décimal, y los númericos enteros y reales.

3. ¿Qué diferencia existe entre TRUNCATE y DELETE?(valor .85)

4. ¿Para qué se utiliza el atributo UNIQUE?(valor .85)

    Se usa en los campos que requieran datos que no se puedan, ni se deban repetir.

5. ¿Qué diferencia hay entre los tipos de datos VARCHAR y CHAR? (valor .85)

    CHAR es un comando que específica una cadena de carácteres con una determinada finitud en su ingreso de información, y VARCHAR es también el ingreso de unad cadena     de carácteres pero con la peculiaridad de que esta es de tipo variable. 

6. Defina brevemente el significado de las siglas SQL(valor .85)

    Structured Query Language. es el lenguaje utilizado para las bases de datos relacionales con el que a través de comandos nos permite seleccionar, insertar,             actualizar y ubicar los datos, y mucho más como la creación de bases de datos.

7. Defina brevemente qué es MySQL WorkBench (valor .85)

     MySQL Workbench es un software libre que funciona como un editor visual de base de datos herramienta que se usa en la creación y edición de diagramas, esquemas y      consultas.
  
## Práctica 5.
### Gestores de base de datos

Objetivo: Categorizar los distintos gestores de base de datos que existen y señalar las
ventajas y desventajas

Evaluación: Conoce los tipos de gestores de base de datos 3 puntos.

Domina sus diferencias de los gestores de base de datos mencionados 3 puntos

Ejercicio:

En un mapa conceptual presenta 3 gestores de bases de datos, sus características
principales, las ventajas y desventajas. (valor 6)

![image](https://user-images.githubusercontent.com/91554777/170415427-e2b7321b-a97f-43b0-ac24-6e506c307e6b.png)

## Práctica 6.
### Herramienta en línea y ejercicio necesarios para realizar las prácticas

Creación de base de datos.

Objetivo: Demostrar mediante la creación de una base de datos el uso y la aplicación de
las funciones

Ejercicio: Creación de la base de datos (valor 18 puntos)

### Tienda de informática
![image](https://user-images.githubusercontent.com/91554777/170415101-717bca19-3644-46a9-8a57-8d5940c5d283.png)

#### Diagrama Modelo entidad/relación.

![image](https://user-images.githubusercontent.com/103280092/175645679-72d085b3-5ccf-416c-be07-1c210dc087a1.png)

#### Base de datos para MySQL.

      CREATE DATABASE tienda_tecnología;
      USE tienda_tecnología;

      CREATE TABLE producto (
      código_producto VARCHAR(10) PRIMARY KEY,
      nombre VARCHAR(100) NOT NULL,
      precio FLOAT UNSIGNED NOT NULL
      );

      INSERT INTO producto VALUES ('DD-23','Disco duro SATA3 1TB',86.99);
      INSERT INTO producto VALUES ('MM-34','Memoria RAM DDR4 8GB',120.6);
      INSERT INTO producto VALUES ('DD-98','Disco SSD 1TB',150.99);
      INSERT INTO producto VALUES ('MM-98','GeForce GTX 1050Ti',185.7);
      INSERT INTO producto VALUES ('MM-23','GeForce GTX 1080 xtreme',755.6);
      INSERT INTO producto VALUES ('MT-12','Monitor 24 LED Full HD',202.1);
      INSERT INTO producto VALUES ('MT-08','Monitor 27 LED Full HD',245.99);
      INSERT INTO producto VALUES ('LP-19','Portátil Yoga 520',559.2);
      INSERT INTO producto VALUES ('LP-11','Portátil Ideapad 320',444.2);
      INSERT INTO producto VALUES ('IM-56','Impresora HP Deskjet 3720',59.99);
      INSERT INTO producto VALUES ('IP-54','Impresora HP Laserjet Pro M26nw',180.3)

      CREATE TABLE fabricante (
      id_fabricante INT AUTO_INCREMENT PRIMARY KEY,
      nombre_marca VARCHAR(50) NOT NULL
      );

      INSERT INTO fabricante VALUES (01,'ASUS');
      INSERT INTO fabricante VALUES (02,'CRUCIAL');
      INSERT INTO fabricante VALUES (03,'GIGABYTE');
      INSERT INTO fabricante VALUES (04,'HP');
      INSERT INTO fabricante VALUES (05,'LENOVO');
      INSERT INTO fabricante VALUES (06,'SAMSUNG');
      INSERT INTO fabricante VALUES (07,'SEAGATE')

      CREATE TABLE profab (
      folio BIGINT UNSIGNED NOT NULL,
      fecha DATE NOT NULL,
      cantidad INT UNSIGNED,
      precio_total INT UNSIGNED,
      código_producto1 VARCHAR(10) NOT NULL,
      id_fabricante1 INT NOT NULL,
      FOREIGN KEY (código_producto1) REFERENCES producto (código_producto),
      FOREIGN KEY (id_fabricante1) REFERENCES fabricante (id_fabricante)
      );

https://www.db-fiddle.com/f/f7hdkCgDcoxrx8wdyJNx1i/0
