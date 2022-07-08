## Práctica 8.
### Disparadores (Triggers)

Objetivo: Demostrar las operaciones que se realizan en una base de datos.

Ejercicio: Crea una base de datos llamada test que contenga una tabla llamada
alumnos con las siguientes columnas. (valor 18)

Evaluación:

Creación de la base de datos : 9 puntos.

Creación de los Disparadores(Triggers): 9 puntos.

Tabla alumnos:

● id (entero sin signo)

● nombre (cadena de caracteres)

● apellido1 (cadena de caracteres)

● apellido2 (cadena de caracteres)

● nota (número real)

      CREATE DATABASE Test;
      USE Test;

      CREATE TABLE Alumnos(
        ID_Alumno INT UNSIGNED PRIMARY KEY,
        nombre VARCHAR(50),
        apellido_paterno VARCHAR(50),
        apellido_materno VARCHAR(50),
        nota FLOAT
      );

      CREATE TABLE Registros(
        Id_regristo INT AUTO_INCREMENT PRIMARY KEY,
        Accion VARCHAR (200),
        Fecha TIMESTAMP DEFAULT CURRENT_TIMESTAMP
       );

Una vez creada la tabla escriba dos triggers con las siguientes características:

● Trigger 1: trigger_check_nota_before_insert

  o Se ejecuta sobre la tabla alumnos.
  
  o Se ejecuta antes de una operación de inserción.
  
  o Se almacena la leyenda 'se ingreso un registro'

      
      DELIMITER //
      CREATE TRIGGER trigger_check_Alumnos_before_insert BEFORE INSERT ON Alumnos
      FOR EACH ROW BEGIN
      INSERT INTO Registros(Accion) VALUES ('Se ingresó un registro');
      END//
      DELIMITER ;


● Trigger2 : trigger_check_nota_before_update
  o Se ejecuta sobre la tabla alumnos.
  
  o Se ejecuta antes de una operación de actualización.
  
  o Se ingresa la leyenda 'se modifico un regisstro'
  
      DELIMITER //
      CREATE TRIGGER trigger_check_Alumnos_before_update BEFORE UPDATE ON Alumnos
      FOR EACH ROW BEGIN
      INSERT INTO Registros(Accion) VALUES ('Se modificó un registro');
      END//
      DELIMITER ;

Una vez creados los triggers escribe varias sentencias de inserción y actualización
sobre la tabla alumnos y verifica que los triggers se están ejecutando
correctamente.

##### Mi ejercicio en DB-FIDDLE: https://www.db-fiddle.com/f/k45om91axqCUMV4qYvYv9t/1



