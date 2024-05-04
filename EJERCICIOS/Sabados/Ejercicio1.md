# VERSION 1

![image](https://github.com/escuelaDeCodigoMargaritaMaza/Base_de_Datos/assets/91554777/45cad88d-d460-4c04-aadd-1af9ddedb787)


     CREATE DATABASE pasteleria;
      CREATE DATABASE papeleria;
      CREATE DATABASE tienda;
      
      USE pasteleria;
      
      /*ELIMINAR LAS OTRAS BASES*/ 
      DROP DATABASE papeleria;
      DROP DATABASE tienda;
      
      /*CREAR TABLA*/
      CREATE TABLE cliente(
         codigo_cliente CHAR(4) PRIMARY KEY,
         nombre_cliente VARCHAR(10),
         apellido_paterno_cliente VARCHAR(10),
         apellido_materno_cliente VARCHAR(10),
         telefono_cliente CHAR(10),
         correo_cliente VARCHAR(10)	
      );
      
      
      /*MODIFICAMOS correo para la longitud*/
      ALTER TABLE cliente 
      CHANGE correo_cliente correo_cliente VARCHAR(30);
      
      
      INSERT INTO cliente VALUES('CL01','Juan','Pérez','González','5587541236','juangonzalez@aol.com');
      
      
      CREATE TABLE proveedor(
        codigo_proveedor CHAR(4)PRIMARY KEY,
        nombre_proveedor VARCHAR(10)
      );
      
      CREATE TABLE categoria_prov(
        codigo_categoria CHAR(4)PRIMARY KEY,
        nombre_categoria VARCHAR(10),
        codigo_proveedor2 CHAR(4),
        FOREIGN KEY (codigo_proveedor2) REFERENCES proveedor(codigo_proveedor)
      );
      
      CREATE TABLE producto(
        codigo_producto CHAR(4) PRIMARY KEY,
        nombre_producto VARCHAR(10),
        precio_producto DOUBLE,
        codigo_proveedor1 CHAR(4),
        FOREIGN KEY (codigo_proveedor1) REFERENCES proveedor(codigo_proveedor)
      );
      
      
      CREATE TABLE nota(
       codigo_cliente1 CHAR(4),
       codigo_producto1 CHAR(4),
       FOREIGN KEY (codigo_cliente1) REFERENCES cliente(codigo_cliente),
       FOREIGN KEY (codigo_producto1) REFERENCES producto(codigo_producto)
      );


# VERSION 2

![image](https://github.com/escuelaDeCodigoMargaritaMaza/Base_de_Datos/assets/91554777/5943b436-a663-43a6-93fd-7ad2d226419f)

