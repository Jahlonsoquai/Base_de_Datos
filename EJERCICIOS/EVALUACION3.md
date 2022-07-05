
## Práctica 4
### Data warehouse

Objetivo: Demostrar la identificación de los elementos que componen data warehouse y
su esquema

Ejercicio:

1. ¿Qué es un DataWarehouse?(valor 2)

Es un tipo de sistema de gestión de datos diseñado para habilitar y dar soporte a las tareas de inteligencia empresarial (BI), especialmente las analíticas. Se han diseñado para realizar consultas y tareas de análisis, y suelen contener grandes cantidades de datos históricos. A menudo, la información dentro de un data warehouse proviene de una amplia gama de fuentes, como los archivos de registro de aplicaciones o las aplicaciones de transacción; el almacén de datos centraliza y fusiona de esas múltiples fuentes la gran cantidad de datos de variables, de las cuales permite a las organizaciones analizar y extraer un valor significativo.          
          
2. Realiza un diseño del modelo en estrella (valor 2)

3. Realiza un diseño del modelo copo de nieve (valor 2)


## Práctica 7
### Funciones en SQL
Objetivo: Demostrar el uso y aplicación en una base de datos para mejorar la gestión

#### Ejercicio:

La liga de la base es: https://www.db-fiddle.com/f/f7hdkCgDcoxrx8wdyJNx1i/3

1. Calcula el número total de productos que hay en la tabla productos. (valor 4.5)

          USE tienda_tecnología;
          SELECT COUNT(código_producto)
          FROM producto;      

2. Muestra el número total de productos que tiene cada uno de los fabricantes. El listado
también debe incluir los fabricantes que no tienen ningún producto. El resultado
mostrará dos columnas, una con el nombre del fabricante y otra con el número de
productos que tiene. Ordene el resultado descendentemente por el número de
productos. (valor 4.5)

          USE tienda_tecnología;
          SELECT nombre_marca, COUNT(nombre_marca)
          FROM fabricante
          INNER JOIN profab ON profab.id_fabricante1=fabricante.id_fabricante 
          INNER JOIN producto ON producto.codigo_producto=profab.codigo_producto1
          GROUP BY (nombre_marca)
          ORDER BY (COUNT(nombre_marca)) DESC;


3. Muestra el precio máximo, precio mínimo y precio medio de los productos de cada
uno de los fabricantes. El resultado mostrará el nombre del fabricante junto con los
datos que se solicitan. (valor 4.5)

          USE tienda_tecnología;
          SELECT nombre_marca, MAX(precio), MIN(precio), AVG(precio)
          FROM producto
          INNER JOIN profab ON producto.codigo_producto=profab.codigo_producto1
          INNER JOIN fabricante ON profab.id_fabricante1=fabricante.id_fabricante
          GROUP BY (nombre_marca)
          ORDER BY (MAX(precio)) ASC;

4. Muestra el nombre de cada fabricante, junto con el precio máximo, precio mínimo,
precio medio y el número total de productos de los fabricantes que tienen un precio
medio superior a 200€. Es necesario mostrar el nombre del fabricante. (valor 4.5)

          USE tienda_tecnología;
          USE tienda_tecnología;
          SELECT nombre_marca, COUNT(nombre_marca), MAX(precio), MIN(precio), AVG(precio)
          FROM producto
          INNER JOIN profab ON producto.codigo_producto=profab.codigo_producto1
          INNER JOIN fabricante ON profab.id_fabricante1=fabricante.id_fabricante
          GROUP BY (nombre_marca)
          HAVING MAX(precio)>200;

