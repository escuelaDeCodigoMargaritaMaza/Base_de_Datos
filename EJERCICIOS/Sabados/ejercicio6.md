    CREATE DATABASE tienda_tecnología;
    USE tienda_tecnología;
    
    CREATE TABLE fabricante (
      codigo_fabricante INT AUTO_INCREMENT PRIMARY KEY,
      nombre_marca VARCHAR(100)
    );
    
    INSERT INTO fabricante VALUES (1,'Asus');
    INSERT INTO fabricante VALUES (2,'Lenovo');
    INSERT INTO fabricante VALUES (3,'HP');
    INSERT INTO fabricante VALUES (4,'Samsung');
    INSERT INTO fabricante VALUES (5,'Segeate');
    INSERT INTO fabricante VALUES (6,'Crucial');
    INSERT INTO fabricante VALUES (7,'Gigabyte');
    INSERT INTO fabricante VALUES (8,'Huawei');
    INSERT INTO fabricante VALUES (9,'Xiaomi');
    
    CREATE TABLE producto (
      codigo_producto INT PRIMARY KEY,
      nombre_producto VARCHAR(100) NOT NULL,
      precio_producto DOUBLE,
      codigo_fabricante1 INT,
      FOREIGN KEY (codigo_fabricante1) REFERENCES fabricante (codigo_fabricante)
    );
    
    
    INSERT INTO producto VALUES (1,'Disco duro SATA3 1TB',86.99,5);
    INSERT INTO producto VALUES (2,'Memoria RAM DDR4 8GB',120,6);
    INSERT INTO producto VALUES (3,'Disco SSD 1TB',150,4);
    INSERT INTO producto VALUES (4,'GeForce GTX 1050Ti',185,5);
    INSERT INTO producto VALUES (5,'GeForce GTX 1080 xtreme',755,6);
    INSERT INTO producto VALUES (6,'Monitor 24 LED Full HD',202,1);
    INSERT INTO producto VALUES (7,'Monitor 27 LED Full HD',245,1);
    INSERT INTO producto VALUES (8,'Portátil Yoga 520',559,2);
    INSERT INTO producto VALUES (9,'Portátil Ideapad 320',444,2);
    INSERT INTO producto VALUES (10,'Impresora HP Deskjet 3720',59,3);
    INSERT INTO producto VALUES (11,'Impresora HP Laserjet Pro M26nw',180,3);
