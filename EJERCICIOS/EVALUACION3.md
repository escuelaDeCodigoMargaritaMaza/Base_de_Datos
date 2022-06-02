
## Práctica 4
### Data warehouse

Objetivo: Demostrar la identificación de los elementos que componen data warehouse y
su esquema

Ejercicio:

1. ¿Qué es un DataWarehouse?(valor 2)

Data warehouse es un sistema que agrega y combina información de diferentes fuentes en un almacén de datos único y centralizado; consistente para respaldar el análisis empresarial, la minería de datos, inteligencia artificial 

2. Realiza un diseño del modelo en estrella (valor 2)

![image](https://user-images.githubusercontent.com/87988894/171659497-c058b289-5ef6-4e7b-94ff-dcc2b6479a00.png)

3. Realiza un diseño del modelo copo de nieve (valor 2)

![image](https://user-images.githubusercontent.com/87988894/171660521-ac2dcb7b-3f82-4290-a1d0-7fa829ccdb80.png)



## Práctica 7
### Funciones en SQL
Objetivo: Demostrar el uso y aplicación en una base de datos para mejorar la gestión

Ejercicio:

1. Calcula el número total de productos que hay en la tabla productos. (valor 4.5)

![image](https://user-images.githubusercontent.com/87988894/171661124-1ce484dd-200c-4336-8dad-8dcc6bc54223.png)

![image](https://user-images.githubusercontent.com/87988894/171661233-baf42a39-8984-43d9-9905-c7da6b3744c6.png)



2. Muestra el número total de productos que tiene cada uno de los fabricantes. El listado
también debe incluir los fabricantes que no tienen ningún producto. El resultado
mostrará dos columnas, una con el nombre del fabricante y otra con el número de
productos que tiene. Ordene el resultado descendentemente por el número de
productos. (valor 4.5)

![image](https://user-images.githubusercontent.com/87988894/171667409-025f2a6b-77cf-4037-a4fd-22aa24fd0b29.png)


![image](https://user-images.githubusercontent.com/87988894/171667496-b361448b-ed39-48d8-ba3d-11ef9bc36af7.png)


3. Muestra el precio máximo, precio mínimo y precio medio de los productos de cada
uno de los fabricantes. El resultado mostrará el nombre del fabricante junto con los
datos que se solicitan. (valor 4.5)

![image](https://user-images.githubusercontent.com/87988894/171670532-3bcd90e3-6ddd-4e0d-b92c-293d7f13804b.png)

![image](https://user-images.githubusercontent.com/87988894/171670685-a2a6e01b-2352-499a-91d0-bac7caa0d786.png)


4. Muestra el nombre de cada fabricante, junto con el precio máximo, precio mínimo,
precio medio y el número total de productos de los fabricantes que tienen un precio
medio superior a 200€. Es necesario mostrar el nombre del fabricante.(valor 4.5)

![image](https://user-images.githubusercontent.com/87988894/171723763-5975a7d0-5207-4462-b289-4c10bbbbd141.png)

![image](https://user-images.githubusercontent.com/87988894/171723870-46d117c4-0cb5-4625-aec8-1c2c9f532306.png)

https://www.db-fiddle.com/f/aoMPqbEVc4tDarFwDNZdcQ/3

## Práctica 8.
### Disparadores (Triggers)

Objetivo: Demostrar las operaciones que se realizan en una base de datos.

Ejercicio: Crea una base de datos llamada test que contenga una tabla llamada
alumnos con las siguientes columnas. (valor 18)

Evaluación:

Creación de la base de datos : 9 puntos.

Creación de los Disparadores(Triggers): 9 puntos.

Tabla alumnos:

● id (entero sin signo)

● nombre (cadena de caracteres)

● apellido1 (cadena de caracteres)

● apellido2 (cadena de caracteres)

● nota (número real)

Una vez creada la tabla escriba dos triggers con las siguientes características:

● Trigger 1: trigger_check_nota_before_insert

  o Se ejecuta sobre la tabla alumnos.
  
  o Se ejecuta antes de una operación de inserción.
  
  o Si el nuevo valor de la nota que se quiere insertar es negativo, se guarda
  como 0.
  
  o Si el nuevo valor de la nota que se quiere insertar es mayor que 10, se
  guarda como 10.
  
  ![image](https://user-images.githubusercontent.com/87988894/171730976-993f9e41-4d45-4c91-8918-99e40ef1cc20.png)


● Trigger2 : trigger_check_nota_before_update
  o Se ejecuta sobre la tabla alumnos.
  
  o Se ejecuta antes de una operación de actualización.
  
  o Si el nuevo valor de la nota que se quiere actualizar es negativo, se guarda
  como 0.
  
  o Si el nuevo valor de la nota que se quiere actualizar es mayor que 10, se
  guarda como 10.
  
  ![image](https://user-images.githubusercontent.com/87988894/171731099-97ffbf2d-a1e2-4264-9f0f-623fc7e857a9.png)

  
  https://www.db-fiddle.com/f/3DHcu9chMhtnRhhBZnTh8H/2
  
Una vez creados los triggers escribe varias sentencias de inserción y actualización
sobre la tabla alumnos y verifica que los triggers se están ejecutando
correctamente.
