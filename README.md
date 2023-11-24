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


