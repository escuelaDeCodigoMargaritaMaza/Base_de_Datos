<img width="440" alt="image" src="https://github.com/user-attachments/assets/b8097685-cd4a-45db-becd-3ab36bbbafa7">
<img width="760" alt="image" src="https://github.com/user-attachments/assets/358ae14c-b661-4836-907e-46726d5a8519">
<img width="625" alt="image" src="https://github.com/user-attachments/assets/75774fe3-f779-4b0d-95cf-70c764028bd7">

# SQL
## DDL definicion
* CREATE
*      - DATABASE (NOMBRE DE LA BASE)
*      - TABLE
*  
* USE (NOMBRE DE LA BASE)


      CREATE DATABASE empresaX;
      USE empresaX;
      CREATE TABLE sucursal(
      	codigo_sucursal CHAR(5) PRIMARY KEY,
          direccion_sucursal VARCHAR(20),
          tel_sucursal CHAR(10),
          correo_sucursal VARCHAR(50)
      );
      CREATE TABLE provedor(
          codigo_provedor CHAR(5) PRIMARY KEY,
          nombre_provedor VARCHAR(20) NOT NULL,
          direccion_provedor VARCHAR(200),
          tel_provedor CHAR(10),
          correo_provedor VARCHAR(20),
          tipo_provedor VARCHAR(20)
      );
      CREATE TABLE cliente(
      	codigo_cliente CHAR(5) PRIMARY KEY,
          nombre_cliente VARCHAR(50) NOT NULL,
          direccion_cliente VARCHAR(200),
          tel_cliente CHAR(10),
          correo_cliente VARCHAR(50),
          codigo_sucursal1 CHAR(5),
          FOREIGN KEY (codigo_sucursal1) REFERENCES sucursal (codigo_sucursal)
      );
      CREATE TABLE producto(
      	codigo_producto CHAR(5) PRIMARY KEY,
          nombre_producto VARCHAR(20) NOT NULL,
          precio_producto DOUBLE UNSIGNED,
          existencia_producto INT UNSIGNED,
          descripcion_producto VARCHAR(200),
          codigo_provedor1 CHAR(5),
          FOREIGN KEY (codigo_provedor1) REFERENCES provedor (codigo_provedor)
      );
      CREATE TABLE categoria(
      	codigo_categoria CHAR(5) PRIMARY KEY,
          nombre_categoria VARCHAR(20) NOT NULL,
          descripcion_categoria VARCHAR(50),
          codigo_provedor2 CHAR(5),
          FOREIGN KEY (codigo_provedor2) REFERENCES provedor(codigo_provedor)
          
      );

        CREATE TABLE empleado(
      	codigo_empleado CHAR(5) PRIMARY KEY,
          nombre_empleado VARCHAR(50) NOT NULL,
          direccion_empleado VARCHAR(200),
      	tel_empleado CHAR(10),
          correo_empleado VARCHAR(20),
          codigo_sucursal2 CHAR(5),
          FOREIGN KEY (codigo_sucursal2) REFERENCES sucursal(codigo_sucursal)
      );

        CREATE TABLE venta(
      	codigo_cliente1 CHAR(5),
          codigo_producto1 CHAR(5),
          fecha_compra DATE,
          cantidad INT,
          total DOUBLE,
          FOREIGN KEY (codigo_cliente1) REFERENCES cliente(codigo_cliente),
          FOREIGN KEY (codigo_producto1) references producto(codigo_producto)
      );

<img width="259" alt="image" src="https://github.com/user-attachments/assets/c930b6e2-0b93-4042-96a1-d65b13a796e1">

      /* AGREGAR A LA TABLA empleado LA EDAD */
      ALTER TABLE empleado
      ADD edad_empleado INT;
      
      /*CAMBIAR TAMAÑO DE LA DIRECCION DE SUCURSAL*/
      ALTER TABLE sucursal
      CHANGE direccion_sucursal direccion_sucursal VARCHAR(200);


      ALTER TABLE venta
      RENAME nota_venta;
      
      ALTER TABLE provedor
      DROP tipo_provedor;
      
      /*DROP TABLE cliente;*/
      
      /*DROP DATABASE empresaX*/
      /*INSERTAR DATOS*/


      INSERT INTO sucursal VALUES('A0001','Calle 1 num 2 colonia centro, alcaldia AZC, CP02200','5566447788','sucursal1@empresax.com');


https://www.db-fiddle.com/f/rLRxgy9kynr2oiV4s5WNHe/0
