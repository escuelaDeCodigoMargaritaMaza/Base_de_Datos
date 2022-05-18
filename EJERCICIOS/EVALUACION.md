## Práctica 1.

1. Introducción a base de datos

Objetivo: Identificar el nivel de comprensión de los conceptos de base de datos,
mediante preguntas abiertas.
 
Preguntas:

1. ¿Cuáles son las cinco funciones principales del administrador de bases de datos?



-asegurar funcionamiento de base de datos

-retencion de datos

-evitar perdida de datos

-Solucionar incidencias y pérdidas de datos

-Asegurar la seguridad de los datos

(valor 1.5)

2. Indíque cinco responsabilidades del sistema gestor de bases de datos 


-Instalar, configurar y gestionar bases de datos.

-Dar soporte al equipo de desarrollo, seguridad informática y redes.

-Definir el esquema del diccionario de datos.

-Especificar restricciones de integridad para asegurar los datos.

-Garantizar la alta disponibilidad de la base de datos.

(valor 1.5)

3. En una BD al usuario del sistema se le brindarán recursos para realizar diversas
operaciones sobre estos archivos, tales como:

-crear cuentas 

-almacenamiento de datos

-modificacion de datos

-transeferencias



(valor 1.5)

4. ¿Qué es un Sistema de Información?

Es sin sistema de almacenacion y ordenacion de datos listos para su uso 
  
  (valor 1.5)

## Práctica 2.

2. Diseño de un modelo relacional

Objetivo: Representar desde un modelo entidad relación un problema


Ejercicio:

Tenemos que diseñar una base de datos sobre proveedores y disponemos de la siguiente
información:

Realiza el modelo entidad relación. 

(valor 6)

Tenemos esta información sobre una cadena editorial:

● La editorial tiene varias sucursales, con su domicilio, teléfono y un código de
sucursal.

● Cada sucursal tiene varios empleados, de los cuales tendremos su nombre,
apellidos, NIF y teléfono. Un empleado trabaja en una única sucursal.

● En cada sucursal se publican varias revistas, de las que almacenaremos su título,
número de registro, periodicidad y tipo.

● Una revista puede ser publicada por varias sucursales.

● La editorial tiene periodistas (que no trabajan en las sucursales) que pueden
escribir artículos para varias revistas. Almacenaremos los mismos datos que para
los empleados, añadiendo su especialidad.

● También es necesario guardar las secciones fijas que tiene cada revista, que
constan de un título y una extensión.

● Para cada revista, almacenaremos información de cada ejemplar, que incluirá la
fecha, número de páginas y el número de ejemplares vendidos.



lista
-sucursal
-empleos
-revistas
-secciones
-ejemplares

caracteristicas

sucursal:domicilio, teléfono y un código desucursal
empleados:nombre,apellidos, NIF y teléfono
revistas:título,número de registro, periodicidad y tipo
periodistas:nombre,apellidos, NIF, teléfono y especialidad
secciones:titulo y extencion
ejeplares:fecha, número de páginas y el número de ejemplares vendidos


![image](https://user-images.githubusercontent.com/87988894/169089389-465c5411-42f0-48ac-9681-c3922a11efe4.png)

