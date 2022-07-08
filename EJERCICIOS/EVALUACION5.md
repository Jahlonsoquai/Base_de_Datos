## Práctica 9.
### Operaciones en una base de datos.
Objetivo: Demostrar las operaciones que se realizan en una base de datos, aplicar el modelo relacional y el lenguaje SQL

Evaluación: Para poder tener correcto cada ejercicio deberán de mostrar el resultado que se da en cada respuesta.

Lista el nombre de todos los productos que hay en la tabla producto.


1. Lista los nombres y los precios de todos los productos de la tabla producto.

        USE tienda_tecnología;
        SELECT nombre, precio 
        FROM producto;

![image](https://user-images.githubusercontent.com/103280092/177921889-ba7922bb-393b-4355-9434-48e2e2584c8b.png)


2. Lista todas las columnas de la tabla producto.

        USE tienda_tecnología;
        SELECT*FROM producto;

![image](https://user-images.githubusercontent.com/103280092/177921647-ab3bb68f-9362-4895-babd-fe271a33cfb6.png)


3. Devuelve una lista con el nombre del producto, precio y nombre de fabricante de
todos los productos de la base de datos.

        USE tienda_tecnología;
        SELECT nombre, precio, nombre_marca
        FROM producto
        INNER JOIN profab ON producto.codigo_producto=profab.codigo_producto1
        INNER JOIN fabricante ON profab.id_fabricante1=fabricante.id_fabricante;

![image](https://user-images.githubusercontent.com/103280092/177922494-c77c722b-fa57-4517-89c0-f998373600e2.png)

Subconsultas (En la cláusula WHERE)
1. Devuelve todos los productos del fabricante Lenovo. (Sin utilizar INNER
JOIN).

        
2. Devuelve todos los datos de los productos que tienen el mismo precio que el
producto más caro del fabricante Lenovo. (Sin utilizar INNER JOIN).



3. Lista el nombre del producto más caro del fabricante Lenovo.
