# Conexion a bases de datos MySQL
## 1)- Levantar Apache en linux 
Esto lo tendremos que hacer para poder usar PhpMyAdmin y asi tener una interfaz grafica para la administracion de bases de datos

 1. systemctl star httpd
 2. systemctl status httpd
 3. systemctl enable httpd
 4. systemctl status httpd
Luego entramos en el localhost desde el navegador y phpmyadmin
## 2)-Configuracion del IDE
Aca intentamos con IntelIJ pero no pudimos asi que migramos al netbeans
 - [ ] Creamos un proyecto java Maven
 - [ ] Instalamos las Dependencias de MySQL connector
 - [ ] Conectamos la Base de Datos introduciendo usuario y contraseña.

## 3)-Creacion del proyecto segun modelo de capas 
Creamos en el paquete fuente los paquetes correspondientes a las capas y a partir de aca vamos generando las clase, objetos y los metodos para una correcta implementacion del CRUD

 - Capa Logica
	 - 
	 - Clase Alumno
		 - Propiedades
		 - Constructores
		 - Getters y Setters
		 - Anotattions
	 - Controlador Logico
		 - Es la clase que se contiene los metodos para poder interpretar las request que provienen de la interfaz grafica, esto quiere decir que son requerimientos por el mismo ususario 
 - Capa Persistencia
	 - 
	 - AlumnoJPAControler
		 - Es la clase que ae crea automaticamente cuando hacemos la configuracion con las anotation y el JPA Persistence, contiene metodos que utilizaemos para el CRUD y algunas busquedas
	 - Controlador de Persistencia 
		 - Se encarga de controlar cada una de las instancias creadas por la controladora logica y de comunicarse con la base de datos
		  
 - Capa IGU
	 - 
	 - Aca 

## Create

#### Basicamente todo se comporta como una cadena
- instancio un objeto de tipo logica en el main, asi puedo usar sus metodos.
- instancio un objeto de tipo alumno, le paso sus paamteros y etc.
- en main le paso al metodo crearAlumno correspondiente a la clase logica el objeto alumno que cree.
- el metodo crearAlumno de la clase logica puede no existir, en ese caso al momento de pasarle se crea automaticamente en logica 


- Instancio objetos de la clase persistencia para poder usar sus metodos en la clase logica
- Creo el metodo crear, pasandole un parametro del tipo de mi Entidad en la DB, este metodo le pasa el parametro a un metodo del mismo nombre pero de persistencia, y le pasa el mismo parametro 
- Instancio un objeto del tipo JPA unit en la capa persistencia, para asi poder usar sus metodos
- Al crear el metodo crear en logica, se me crea el metodo crear en persistencia,  el cual recibe el mismo dato de tipo ENTITY ()el metodo crear de la persistencia, debe saber a que llamar JPA llamar en caso de tener varias tablas, esto se hace especificando el ENTITY), este metodo llama al metodo create de la JPA unit el cual se encarga de crear el objeto en la tabla.

Los el dato que le paso a logica puede venir del main el cual lo paso yo mismo, pero lo ideal seria que IGU le pase los datos los cuales son introducidos por el usuario y que igu lo mande directamente a logica sin pasar por main y luego sabemos como es la cadena . 

Los metodos que creamos y demas son del main, asi que hayq eu tener en cuenta que al momento de comprobar las otras acciones del crus, estas comprobaciones podrain interferir entre si
Para que no haya interferencia entre comprobaciones, deberia crear 4 alumnos, y aplicarle a cada uno una opercaion distinta, asi cuando corro el programa no hay interferencias.

## Delete 
Es exactamente igual solo que en vez de pasar un objeto, solo paso una propiedad del objeto, esa propiedad debe ser la primary key en la DB.
Ademas de eso al momento de crear el metodo eliminar en la persistencia, y llamar a JPA, me va a decir que lo mediante un try catch por si paso mal el valor de la primary key.

## Update
Es como el create, tambien le debo pasar un objeto alumno entero. Lleva un try/catch en persistencia por si me confundo y mando algo mal.



