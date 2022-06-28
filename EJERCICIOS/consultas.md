En la BD utilizada en clase realiza las siguientes consultas:

https://www.db-fiddle.com/f/or2rUwTQ6f2ozgPbtx1dMi/1

* La tabla empleado:

      USE editorial;
      SELECT * FROM empleados;

* Los titulos de las revistas:
      
      USE editorial;
      SELECT titulo FROM  revista;

* Los nombres, apellidos y especialidad de los periodostas:

      USE editorial;
      SELECT nombre_periodista,apellidos_periodista,especialidad FROM periodistas;

* Muestra los empleados que estan en x sucursal:
      
      USE editorial;
      SELECT nombre_empleado, apellidos_empleado FROM empleados
      INNER JOIN sucursal ON empleados.codigo_de_sucursal1=sucursal.codigo_de_sucursal
      WHERE codigo_de_sucursal=01;

* Muestra que periodistas colaboraron en x revista y en que sucursal se publico la revista:

      USE editorial;
      SELECT nombre_periodista, apellidos_periodista, titulo, codigo_de_sucursal FROM periodistas 
      INNER JOIN trabajan ON periodistas.nif=trabajan.nif1
      INNER JOIN revista ON trabajan.numero_de_registro2=revista.numero_de_registro 
      INNER JOIN publican ON revista.numero_de_registro=publican.numero_de_registro1
      INNER JOIN sucursal ON publican.codigo_de_sucursal2=sucursal.codigo_de_sucursal;

* Muestra que seccion esta en x revista, en que sucursal se imprimio y que empleados estan en esa sucursal.
* En la tabla peridistas muestra solo los que escriban sobre cine
* De la tabla revistas muestra las que sean de publicacion quincenal
* Muestra el nombre de ka revista que se hayan impreso despues del 30 de septiembre del 2021
* Muestra el nombre de la revista que se haya publicado en la sucursal 1 cuyos ejemplares tengan más de 80 páginas.

https://www.db-fiddle.com/f/iAUjGLoFoHtam2pK68Xh1B/1



