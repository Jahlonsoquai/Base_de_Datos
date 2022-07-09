# Proyecto Final de base de datos.
### Indicaciones de lo que se debe realizar

● Diseña el modelo entidad-relación del siguiente problema.

● Crea el script para la base de datos.
Proveedores

Tenemos que diseñar una base de datos sobre proveedores y disponemos de
la siguiente información:

● De cada proveedor conocemos su nombre, dirección, ciudad, provincia y
un código de proveedor que será único para cada uno de ellos.

● Nos interesa llevar un control de las piezas que nos suministra cada
proveedor. Es importante conocer la cantidad de las diferentes piezas
que nos suministra y en qué fecha lo hace. Tenga en cuenta que un
mismo proveedor nos puede suministrar una pieza con el mismo código
en diferentes fechas. El diseño de la base de datos debe permitir
almacenar un histórico con todas las fechas y las cantidades que nos ha
proporcionado un proveedor.

● Una misma pieza puede ser suministrada por diferentes proveedores.

● De cada pieza conocemos un código que será único, nombre, color,
precio y categoría.

● Pueden existir varias categorías y para cada categoría hay un nombre y
un código de categoría único.

● Una pieza sólo puede pertenecer a una categoría.

#### Diagrama Entidad-Relación:

![image](https://user-images.githubusercontent.com/103280092/178081877-3db042e8-6332-43be-9b5e-b4de42edb305.png)

#### Script de BD:

    CREATE DATABASE Proveedores;
    USE Proveedores;

    CREATE TABLE Proveedor(
      ID_Proveedor INT AUTO_INCREMENT PRIMARY KEY,
      Nombre_Proveedor VARCHAR(100) NOT NULL,
      Dirección VARCHAR(100) NOT NULL,
      Ciudad VARCHAR(50) NOT NULL,
      Provincia VARCHAR(50)
    );

    CREATE TABLE Categoria(
      ID_Categoria INT AUTO_INCREMENT PRIMARY KEY,
      Nombre_Categoria VARCHAR(50) NOT NULL
    );

    CREATE TABLE Pieza(
      ID_Pza INT AUTO_INCREMENT PRIMARY KEY,
      Nombre_Pza VARCHAR(100) NOT NULL,
      Color VARCHAR(20),
      Precio FLOAT UNSIGNED NOT NULL,
      ID_Categoria1 INT NOT NULL,
      FOREIGN KEY (ID_Categoria1) REFERENCES Categoria (ID_Categoria)
    );

    CREATE TABLE Nota_Suministro(
      Folio VARCHAR(100),
      Cantidad INT UNSIGNED NOT NULL,
      Fecha_Distribucion DATE NOT NULL,
      ID_Proveedor1 INT NOT NULL,
      ID_Pza1 INT NOT NULL,
      FOREIGN KEY (ID_Proveedor1) REFERENCES Proveedor (ID_Proveedor),
      FOREIGN KEY (ID_Pza1) REFERENCES Pieza (ID_Pza)
    );
 

En: https://www.db-fiddle.com/f/ayY2BUaESRnuLSGauZCutt/0
