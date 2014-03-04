Base de datos:

Dentro de la carpeta EjercicioSQL tenemos los archivos correspondientes al ejercicio 'The computer store'. 
DB1.sql contiene las intrucciones para crear la base de datos que vamos a usar, para ello ejecutar "source rutaDelArchivo".
EntregaDB.txt contiene los comandos de las consultas del ejercicio.

JDBC:

Para el ejercicio de JDBC se ha tenido que crear una base de datos, para ello se han usado los comandos que se nos proporcionan en la web del tutorial:

create database feedback;
use feedback; 

CREATE USER sqluser IDENTIFIED BY 'sqluserpw'; 

grant usage on *.* to sqluser@localhost identified by 'sqluserpw'; 
grant all privileges on feedback.* to sqluser@localhost; 

CREATE TABLE COMMENTS (id INT NOT NULL AUTO_INCREMENT, 
    MYUSER VARCHAR(30) NOT NULL,
    EMAIL VARCHAR(30), 
    WEBPAGE VARCHAR(100) NOT NULL, 
    DATUM DATE NOT NULL, 
    SUMMARY VARCHAR(40) NOT NULL,
    COMMENTS VARCHAR(400) NOT NULL,
    PRIMARY KEY (ID));

INSERT INTO COMMENTS values (default, 'lars', 'myemail@gmail.com','http://www.vogella.com', '2009-09-14 10:33:11', 'Summary','My first comment'); 

Una vez creada la base de datos podemos ejecutar el proyecto y nos mostara las consultas por pantalla.