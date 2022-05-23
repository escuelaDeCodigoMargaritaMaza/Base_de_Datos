1. Instalación del gestor de base de datos MYSQL

Ingresamos al siguiente link : https://dev.mysql.com/downloads/

Damos clip en el enlace MYSQL Community Server

![image](https://user-images.githubusercontent.com/91554777/169728244-274da346-94cb-42a9-8c1f-a201cc8fe0af.png)

Nos llevará a la página siguiente para descargar el archivo ejecutable
para poder hacer la instalación.
Es importante saber si nuestra computadora es de 32 bits o 64 bits el
sistemas web determina cual es el ejecutable que debemos descargar.

![image](https://user-images.githubusercontent.com/91554777/169728266-a85dd066-4685-4399-9ef0-32552315496e.png)

Oprimes el siguiente botón.

Te mandara a la siguiente página.

![image](https://user-images.githubusercontent.com/91554777/169728305-0b844e16-23d7-4b52-9254-845fb6e27bcb.png)

Seleccionar la opción marcada nos mandara a la siguiente página

![image](https://user-images.githubusercontent.com/91554777/169728337-ef2baccd-f7f5-4194-b381-e2f6b634586d.png)

Se descarga el ejecutable .

![image](https://user-images.githubusercontent.com/91554777/169728368-e7094c74-a99d-42bc-b8e4-812544a2429e.png)

Lo instalamos .

![image](https://user-images.githubusercontent.com/91554777/169728406-83bf6910-7117-4bba-91ad-24fb05ecd9b6.png)

Si le damos a la opción de “Custom” tendremos bastantes opciones para
elegir.
Esta opción está dirigida a usuarios que ya cuentan con experiencia
trabajando en otros gestores de bases de datos. Vamos a ver un poco las
opciones principales de instalación:
MySQL Servers: esta será la herramienta principal y básica si deseamos
utilizar nuestro equipo para convertirlo en un servidor y gestor de bases
de datos. En nuestro caso vamos a instalar este paquete, para poder
realizar la conexión luego mediante el cliente. Por tanto, desplegamos
toda la lista del apartado, y pulsamos en la flecha para mover la opción
hacia la derecha.

![image](https://user-images.githubusercontent.com/91554777/169728440-676180a4-13c0-4b66-863d-bdd2d6bc9385.png)

![image](https://user-images.githubusercontent.com/91554777/169728473-0a81ac80-d908-4149-a43e-470bb1cfd7f8.png)

MySQL Workbench: estará situada en el apartado de “Applications” y
será nuestro cliente de MySQL. Procedemos igual que en el punto
anterior.

![image](https://user-images.githubusercontent.com/91554777/169728502-da72cf63-23a6-496f-bc15-98f68e636749.png)

MySQL Connections: esta opción irá en función de las conexiones que
nosotros queramos realizar. Según los clientes y los lenguajes de
programas que vayamos a utilizar. Lo mejor será instalar todos estos
paquetes por si en un futuro necesitamos alguno de ellos.

![image](https://user-images.githubusercontent.com/91554777/169728555-5572bded-c8bf-420d-8bfd-d0c0c7d998a3.png)

En esta ventana ya se abra instalado todos los paquetes

![image](https://user-images.githubusercontent.com/91554777/169728606-6ec51adf-f858-4c03-8677-1bc11a1d74e5.png)

Veremos todo lo que se instaló.

### 2. Configuración de MySQL

Finalizada la instalación de los módulos será turno de proceder a una
configuración inicial antes de ejecutar los correspondientes servicios.
Pulsamos “Next” y elegimos la primera opción “Standalone MySQL
Server/Classic MySQL Replication”.

![image](https://user-images.githubusercontent.com/91554777/169728653-f66ac100-ea8f-4988-88df-0e3341501d14.png)

La siguiente pantalla es importante, ya que necesitaremos configurar
algunos parámetros como el tipo de equipo que tendremos para SQL,
además de protocolos y puertos TCP por donde se efectuarán las
conexiones remotas al servidor SQL.
Para la configuración de tipo de ordenador tendremos tres opciones
distintas:

● Development Computer: Está orientado a ser un equipo en el que
está instalado el servidor SQL, pero también el cliente para las
consultas de bases de datos. Si nuestro equipo es doméstico y
trabajamos de forma normal en él está será la opción que
debemos elegir.

● Server Computer: esta segunda opción será orientada a
ordenadores utilizados para funciones de servidor, por ejemplo,
servidor web con bases de datos. Dedicated Computer: la tercera
opción es par el caso en que queremos crear un equipo solo y
exclusivamente orientado a bases de datos. Por ejemplo, una
máquina virtual en la que se almacenen nuestras bases de datos.


● La siguiente opción que tendremos que elegir es la del puerto TCP
que utilizaremos para conexiones remotas. Por defecto es el 3306.
La opción que marquemos aquí será el puerto que tendremos que
abrir en nuestro router para establecer las conexiones remotas.
El resto de opciones recomendamos dejarlas por defectos tal y como
están.

![image](https://user-images.githubusercontent.com/91554777/169728695-c1ebdace-2cf5-4d89-a000-b64483d56485.png)

A continuación, debemos elegir la contraseña para conectarnos en el
servidor SQL. Esta configuración la podremos modificar en cualquier
momento desde el propio servidor. No será necesario definir un usuario
específico para administrar la base de datos, ya que por defeco será el
usuario root

![image](https://user-images.githubusercontent.com/91554777/169728737-94da2158-43de-4fc6-a58b-7da5dd83826b.png)

Puede que la base de datos no tenga contraseña.
Finalmente configuraremos el nombre del servicio para MySQL y las
preferencias generales en cuando a inicio del demonio y el uso de
cuentas de usuario.

![image](https://user-images.githubusercontent.com/91554777/169728767-47845ac6-3ae0-445a-87b7-c48c8c7a8391.png)

Para finalizar, en la última pantalla pulsamos en “Execute” para ejecutar
las acciones y activar los servicios correspondientes en el sistema. Todo
debería de haberse completado correctamente. En caso de no ser así,
veremos una x roja en el elemento de la lista y tendremos que ver el log
de error para saber más información acerca de este.

![image](https://user-images.githubusercontent.com/91554777/169728788-00793cc8-4589-48ea-9c2d-6fa868dc5623.png)

Si hemos instalado otros elementos extras como los ejemplos, también
necesitaremos configurarlos. Lo único que tendremos que hacer será
conectar con el servidor mediante el usuario root y la contraseña que
hayamos definido anteriormente

![image](https://user-images.githubusercontent.com/91554777/169728811-0c262f43-0dc3-48e1-a1a2-01b5d8184588.png)

De esta forma habremos finalizado el proceso para instalar MySQL en
Windows 10

3. Conectarnos a MySQL server desde MySQL Workbench

Si durante el proceso hemos instalado el cliente gráfico MySQL
Workbench, se nos abrirá automáticamente tras la instalación para
poder conectarnos a un servidor.

Por defecto, nos aparecerá el enlace de conexión a nuestro propio
equipo en donde tendremos instalado el server. Vamos a suponer que
no tenemos creada ninguna conexión, así veremos cómo configurar una.

Lo primero que tendremos que hacer es pulsar sobre el botón “+” de
“MySQL Connections”

![image](https://user-images.githubusercontent.com/91554777/169728899-87a75586-0db9-427e-b525-0faec7e48a25.png)

Ahora en la ventana que se nos abre tendremos que colocar los
siguientes parámetros:

● Un nombre para la conexión. El que queramos.

● Elegir como protocolo estándar, el TCP/IP.

● En “hostname” tendremos que colocar la dirección IP del servidor.
Si es nuestro propio equipo la IP debe ser 0.0.1. Pero estamos en
una red local, será la dirección IP que tenga asignada en su
tarjeta de red. Si es una conexión remota necesitaremos saber la
dirección externa del de la conexión.

● Puerto de conexión: colocamos el que hayamos configurado
anteriormente.

● Nombre de usuario: en nuestro caso podríamos colocar root o el
que configuramos anteriormente
Cuando este todo, pulsamos en “OK” o en “Test connection” para
comprobar si la conexión es correcta. Nos pedirá la clave y todo debería
de ir correctamente.
Ahora en la ventana que se nos abre tendremos que colocar los siguientes
parámetros:

● Un nombre para la conexión. El que queramos.

● Elegir como protocolo estándar, el TCP/IP.

● En “hostname” tendremos que colocar la dirección IP del servidor. Si es
nuestro propio equipo la IP debe ser 0.0.1. Pero si estamos en una red local,
será la dirección IP que tenga asignada en su tarjeta de red. Si es una
conexión remota necesitaremos saber la dirección externa de la conexión.

● Puerto de conexión: colocamos el que hayamos configurado anteriormente.

● Nombre de usuario: en nuestro caso podríamos colocar root o el que
configuramos anteriormente

Cuando este todo, pulsamos en “OK” o en “Test connection” para comprobar si
la conexión es correcta. Nos pedirá la clave y todo debería de ir correctamente.

![image](https://user-images.githubusercontent.com/91554777/169728962-55f3d8f0-394e-491f-a0bf-33f6039d68e4.png)

En la ventana principal de MySQL Workbench aparecerá la nueva
conexión creada para poder conectarnos con un solo clic. De esta forma
ya estaremos dentro del entorno de gestión de bases de datos de
MySQL.

![image](https://user-images.githubusercontent.com/91554777/169728985-b21e593d-9a20-4f6f-b101-4ccc5562a20c.png)

Colocamos el pasword que escribimos en la configuración .

![image](https://user-images.githubusercontent.com/91554777/169729016-dede8088-2658-4d79-aeed-ce92a0e0f8ce.png)

Esta será la venta si es que todo fue instalado correctamente.
