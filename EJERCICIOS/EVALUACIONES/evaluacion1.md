La editorial tiene varias sucursales, con su domicilio, teléfono y un código de sucursal.

Cada sucursal tiene varios empleados, de los cuales tendremos su nombre, apellidos, NIF y teléfono. Un empleado trabaja en una única sucursal.

En cada sucursal se publican varias revistas, de las que almacenaremos su título, número de registro, periodicidad y tipo.

Una revista puede ser publicada por varias sucursales.

La editorial tiene periodistas (que no trabajan en las sucursales) que pueden escribir artículos para varias revistas. Almacenaremos los mismos datos que para los empleados, añadiendo su especialidad.


<img width="612" alt="image" src="https://github.com/user-attachments/assets/ef12abf2-52ee-46da-9014-8a2ac44ae2d3">


    CREATE DATABASE editorial;
    USE editorial;
    CREATE TABLE sucursal(
    	codigo_sucursal INT PRIMARY KEY,
        domicilio_sucursal VARCHAR(100) NOT NULL,
        tel_sucursal CHAR(10)
    );
    ALTER TABLE sucursal
    CHANGE domicilio_sucursal domicilio_sucursal VARCHAR(500);
    
    CREATE TABLE periodista(
    	NIF_periodista INT PRIMARY KEY,
        nomnbre_periodista VARCHAR(20),
        apellido_periodista VARCHAR(20),
        tel_periodista CHAR(10),
        especialidad VARCHAR(20)
    );
    CREATE TABLE empleado(
    	NIF_empleado INT PRIMARY KEY,
        nombre_empleado VARCHAR(20),
        apellido_empleado VARCHAR(20),
        tel_empleado CHAR(10),
        codigo_sucursal1 INT,
        FOREIGN KEY (codigo_sucursal1) REFERENCES sucursal(codigo_sucursal)
    );
    
    CREATE TABLE revista(
    	numero_registro INT PRIMARY KEY,
        titulo_revista VARCHAR(20),
        tipo_revista VARCHAR(20),
        periodicidad VARCHAR(20),
        codigo_sucursal2 INT,
        FOREIGN KEY (codigo_sucursal2) REFERENCES sucursal(codigo_sucursal)
    );
    
    CREATE TABLE perrevi(
       numero_registro1 INT,
       NIF_periodista1 INT,
       FOREIGN KEY (numero_registro1) REFERENCES revista(numero_registro),
       FOREIGN KEY (NIF_periodista1) REFERENCES periodista(NIF_periodista)
    );
