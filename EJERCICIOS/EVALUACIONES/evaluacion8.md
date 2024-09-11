    CREATE DATABASE EscuelaTrigger;
    USE EscuelaTrigger;
    CREATE TABLE alumno(
    	id_alumno INT PRIMARY KEY,
        nombre_alumno VARCHAR(50),
        apellido_alumno VARCHAR(20),
        nota_alumno DOUBLE
    );
    INSERT INTO alumno VALUES (001,"Juan","Perez", 8.5);
    
    CREATE TABLE registro(
    id_registro INT AUTO_INCREMENT PRIMARY KEY, 
    accion VARCHAR(100),
    fecha TIMESTAMP DEFAULT CURRENT_TIMESTAMP
    );
    
    DELIMITER //
    	CREATE TRIGGER tg_check_nota_before_insert BEFORE INSERT ON alumno
        FOR EACH ROW BEGIN
        INSERT INTO registro(accion) VALUES ('se agrego alumno');
        END//
    DELIMITER ;
    
    INSERT INTO alumno VALUES(002, "Pedro","Martinez",8.2);
    INSERT INTO alumno VALUES(003, "Patricia","Marquez",7.5);
    INSERT INTO alumno VALUES(004, "Paola","Marin",8.5);
    
    SELECT *
    FROM registro;
    
    DELIMITER //
    	CREATE TRIGGER tg_check_nota_before_update BEFORE UPDATE ON alumno
        FOR EACH ROW BEGIN
        INSERT INTO registro(accion) VALUES ('se modifico un alumno');
        END//
    DELIMITER ;
    
    UPDATE alumno
    SET nombre_alumno = "Miguel"
    WHERE id_alumno = 002;
    
    SELECT *
    FROM registro;
    
    DROP TRIGGER tg_check_nota_before_insert;
    DROP TRIGGER tg_check_nota_before_update;
    
    DELIMITER //
    	CREATE TRIGGER tg_check_nota_before_insert BEFORE INSERT ON alumno
        FOR EACH ROW BEGIN
        IF NEW.nota_alumno < 0 THEN
    		SET NEW.nota_alumno = 0;
    	ELSEIF NEW.nota_alumno > 10 THEN
    		SET NEW.nota_alumno = 10;
    END IF;
    
    INSERT INTO registro(accion) VALUES (concat("Se agrego un
    alumno con La nota de:" , NEW.nota_alumno));
    END//
    DELIMITER ;
    
    
    INSERT INTO alumno VALUES(009, "Paola","Marin",-8.5);
    INSERT INTO alumno VALUES(010, "Paola","Marin",18.5);
