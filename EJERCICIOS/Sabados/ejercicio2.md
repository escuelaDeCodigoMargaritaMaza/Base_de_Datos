![image](https://github.com/escuelaDeCodigoMargaritaMaza/Base_de_Datos/assets/91554777/fb853181-5726-4f70-81eb-3e63bd4fd09b)



    CREATE DATABASE pilares;
    USE pilares;
    
    CREATE TABLE usuario (
      folio_usuario CHAR(4) PRIMARY KEY,
      nombre_usuario VARCHAR(5) NOT NULL
    );  
    
    CREATE TABLE taller(
      codigo_taller CHAR(4) PRIMARY KEY,
      nombre_taller VARCHAR(5) NOT NULL
    );
    
    CREATE TABLE grupo(
      folio_usuario1 CHAR(4),
      codigo_taller1 CHAR(4),
      FOREIGN KEY (folio_usuario1) REFERENCES usuario(folio_usuario),
      FOREIGN KEY (codigo_taller1) REFERENCES taller(codigo_taller)
    );
    
    ALTER TABLE usuario
    ADD apellido_paterno_usuario VARCHAR(10);
    ALTER TABLE usuario
    ADD telefono_usuario CHAR(10);
    ALTER TABLE usuario
    ADD correo_usuario VARCHAR(50);
    
    ALTER TABLE taller
    ADD duracion_taller VARCHAR(5);
    
    CREATE TABLE tallerista(
    folio_tallerista CHAR(4) PRIMARY KEY,
    nombre_tallerista VARCHAR(10),
    apellido_paterno_tallerista VARCHAR(10),
    telefono_tallerista CHAR(10),
    correo_tallerista VARCHAR(50),
    codigo_taller2 CHAR(4),
    FOREIGN KEY (codigo_taller2) REFERENCES taller(codigo_taller)
    );
    
    ALTER TABLE grupo
    ADD codigo_grupo CHAR(4),
    ADD horario_grupo VARCHAR(5);
    
    INSERT INTO usuario VALUES ('AA11','Carlos','Sanchez','5578239651','carlossanchez@pilares.com');
    
    ALTER TABLE usuario
    CHANGE nombre_usuario nombre_usuario VARCHAR(10);
    
    INSERT INTO usuario VALUES ('AA12','Andrea','Dominguez','5503258741','andreadominguez@pilares.com'), 
    ('AA13','Andres','Castillo','5502350879','andrescastillo@pilares.com'),
    ('AA14','Carla','Perez','5565498032','carlaperez@pilares.com');
    
    ALTER TABLE taller
    CHANGE duracion_taller duracion_taller VARCHAR(10);
    
    ALTER TABLE taller
    CHANGE nombre_taller nombre_taller VARCHAR(15);
    
    INSERT INTO taller VALUES ('TA01','Carpinteria','4 horas'),
    ('TA02','Computacion','2 horas'),
    ('TA03','Reposteria','4 horas');
    
    ALTER TABLE grupo
    CHANGE horario_grupo horario_grupo CHAR(17);
    
    INSERT INTO grupo VALUES ('AA12','TA01','CA1A','10:00 h - 14:00 h'),
    ('AA14','TA01','CA1A','10:00 h - 14:00 h'),
    ('AA14','TA03','RE1A','14:00 h - 18:00 h'),
    ('AA11','TA02','CO1A','08:00 h - 11:00 h'),
    ('AA12','TA02','CO1A','08:00 h - 11:00 h'),
    ('AA13','TA02','CO1A','08:00 h - 11:00 h');
    
    INSERT INTO tallerista VALUES 
    ('pr01','Manuel','Salinas','5563298704','manuelsalinas@pilares.mx','TA02'),
    ('pr02','Jose','Hernandez','5528756300','josehernandez@pilares.mx','TA01'),
    ('pr03','Fatima','Flores','5547896301','fatimaflores@pilares.mx','TA03');


