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

## MODELO

![image](https://github.com/escuelaDeCodigoMargaritaMaza/Base_de_Datos/assets/91554777/57ea118c-edea-4601-8ea1-ca3db4da34b8)


## SOLUCION PROPUESTA
    
    CREATE DATABASE proveedores;
    
    USE proveedores;
    
    CREATE TABLE proveedor (
      codigo_prov INT PRIMARY KEY,
      nombre_prov VARCHAR (50),
      direccion_prov VARCHAR (100),
      cuidad_prov VARCHAR(20)
      );
      
    CREATE TABLE categoria (
      codigo_categoria INT PRIMARY KEY,
      nombre_categoria VARCHAR (50)
        );
          
    CREATE TABLE pieza (
      codigo_pieza INT PRIMARY KEY,
      nombre_pieza VARCHAR (50),
      color_pieza VARCHAR (20),
      precio_pieza DOUBLE,
      categoria_pieza VARCHAR(20),
      codigo_categoria1 INT,
      FOREIGN KEY (codigo_categoria1) REFERENCES categoria(codigo_categoria)
    );    
      
    CREATE TABLE suministro (
      fecha_suministro TIMESTAMP,
      cantidad_suministro VARCHAR (50),
      codigo_prov1 INT,
      codigo_pieza1 INT,
      FOREIGN KEY (codigo_prov1) REFERENCES proveedor(codigo_prov),
      FOREIGN KEY (codigo_pieza1) REFERENCES pieza(codigo_pieza)
      );  
      
    INSERT INTO proveedor VALUES (111, 'prov01', 'cerrada 25, col. san jose', 'CDMX'); 
    INSERT INTO proveedor VALUES (222, 'prov02', 'cerrada 25, col. san jose', 'CDMX');    
    INSERT INTO proveedor VALUES (333, 'prov03', 'cerrada 25, col. san jose', 'CDMX');    
    INSERT INTO proveedor VALUES (444, 'prov04', 'cerrada 25, col. san jose', 'CDMX');    
    INSERT INTO proveedor VALUES (555, 'prov05', 'cerrada 25, col. san jose', 'CDMX');    
    INSERT INTO proveedor VALUES (666, 'prov06', 'cerrada 25, col. san jose', 'CDMX');    
    INSERT INTO proveedor VALUES (777, 'prov07', 'cerrada 25, col. san jose', 'CDMX');   
    
    INSERT INTO categoria VALUES (1, 'ceramica');
    INSERT INTO categoria VALUES (2, 'carton');
    INSERT INTO categoria VALUES (3, 'madera');
    INSERT INTO categoria VALUES (4, 'metal');    
        
    
    INSERT INTO pieza VALUES ('01', 'pieza01', 'verde', 12.50, 'ceramica', 1);
    INSERT INTO pieza VALUES ('02', 'pieza02', 'azul', 90.00, 'madera', 3);
    INSERT INTO pieza VALUES ('03', 'pieza03', 'morado', 89.50, 'madera', 3);
    INSERT INTO pieza VALUES ('04', 'pieza04', 'blanco', 15.00, 'carton', 2);
    INSERT INTO pieza VALUES ('05', 'pieza05', 'amarillo', 199.00, 'metal', 4);
    INSERT INTO pieza VALUES ('06', 'pieza06', 'gris', 49.00, 'carton', 2);
    INSERT INTO pieza VALUES ('07', 'pieza07', 'rojo', 66.00, 'ceramica', 1);
