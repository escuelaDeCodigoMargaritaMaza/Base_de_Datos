![image](https://github.com/user-attachments/assets/bb334299-8c3e-451d-9d5a-b3beeadd058a)



![image](https://github.com/user-attachments/assets/726207c3-4287-487c-9305-efd357e59c88)

![image](https://github.com/user-attachments/assets/2aa35e40-ed28-4381-b92a-5c44e7bcb4b6)


        CREATE DATABASE evaluacion2;
        USE evaluacion2;
        
        CREATE TABLE fabricante(
        codigo_fabricante INT PRIMARY KEY,
        nombre_fabricante VARCHAR (100)
        );
        
        CREATE TABLE producto(
        codigo_producto INT PRIMARY KEY,
        nombre_producto VARCHAR (100),
        precio_producto DOUBLE,
        codigo_fabricante1 INT,
        FOREIGN KEY (codigo_fabricante1) REFERENCES fabricante(codigo_fabricante)
        );
        
        /*insertar datos*/
        INSERT INTO fabricante VALUES (1,'Asus'); 
        INSERT INTO fabricante VALUES (2,'Lenovo');
        INSERT INTO fabricante VALUES (3,'Hewelett-Packrd');
        INSERT INTO fabricante VALUES (4,'Samsung');
        INSERT INTO fabricante VALUES (5,'Seagate');
        INSERT INTO fabricante VALUES (6,'Crucial');
        INSERT INTO fabricante VALUES (7,'Gigabyte');
        INSERT INTO fabricante VALUES (8,'Huawei');
        INSERT INTO fabricante VALUES (9,'Xiaomi');
        
        SELECT *
        FROM fabricante;
        
        INSERT INTO producto VALUES (1,'Disco Duro SATA3 1TB',86.99,5);
        INSERT INTO producto VALUES (2,'Memoria RAM DDR4 8GB',120,6);
        INSERT INTO producto VALUES (3,'Disco SSD 1TB',150.99,4);
        INSERT INTO producto VALUES (4,'GeForce GTX 1050 Ti',185,7);
        INSERT INTO producto VALUES (5,'GeForce GTX 1080 Xtreme',755,6);
        INSERT INTO producto VALUES (6,'Monitor 24 LED Full HD',202,1);
        INSERT INTO producto VALUES (7,'Monitor 27 LED Full HD',245.99,1);
        INSERT INTO producto VALUES (8,'Portatil Yoga 520',559,2);
        INSERT INTO producto VALUES (9,'Portatil Ideapad 320',444,2);
        INSERT INTO producto VALUES (10,'Impresora HP Deskjet 3720',59.99,3);
        INSERT INTO producto VALUES (11,'Impresora HP Laserjet Pro M26nw',180,3);
