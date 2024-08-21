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
