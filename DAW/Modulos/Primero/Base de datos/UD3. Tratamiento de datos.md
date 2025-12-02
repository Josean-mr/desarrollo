# 4. Tipos de órdenes del lenguaje SQL
[[00. Comandos]]
## <font style="color:salmon">DDL</font>
Es el **lenguaje de descripción de datos** o **lenguaje de definición de datos** que se utiliza para la creación y mantenimiento de la estructura de la base de datos.
- Se definen y modifican los esquemas de las relaciones.
- Se crean o destruyen índices.
- Se eliminan relaciones.
- Se pueden definir vistas y permisos de acceso para los usuarios.
- Permite definir los subesquemas externos, el esquema conceptual y el esquema interno.
## <font style="color:salmon">DML</font>
Es el **lenguaje de manipulación de datos**, que incluye instrucciones para:
- Consultar la base de datos.
- Insertar tuplas.
- Eliminar tuplas.
- Modificar valores de datos.
## <font style="color:green">Sentencias DDL y DML</font>
[Link](https://codigosql.com/blog/sentencias-ddl-y-dml/)
## <font style="color:salmon">DCL</font>
Es el **lenguaje de control de datos**. Son un conjunto de comandos y sentencias que se utilizan para administrar los permisos de acceso y controlar la seguridad de los sistemas gestores de bases de datos.
- Tipos de privilegios:
	- SELECT:
		- Consulta.
	- UPDATE:
		- Actualización.
	- DELETE:
		- Borrado.
- Creación de usuario:
	- CREATE USER.
### <font style="color:orange">Principales comandos</font>:
- <font style="color:#08F; font-weight:bold">GRANT</font>:
	- Para otorgar permisos específicos a los usuarios.
	- <font style="color:green">Ejemplo</font>:
		- `GRANT ALL PRIVILEGES ON Empleado TO Usuario1`
			- Asigna todos los privilegios a Usuario1 de la tabla Empleado.
		- `GRANT SELECT ON Empleado TO Usuario1`
			- Asigna el permiso de consulta a Usuario1 de la tabla Empleado.
- <font style="color:#08F; font-weight:bold">REVOKE</font>:
	- Para revocar permisos.
		- <font style="color:green">Ejemplo</font>:
			- `REVOKE SELECT ON Empleado FROM Usuario1`
				- Revoca el permiso de consulta a Usuario1 de la tabla Empleado.
- <font style="color:#08F; font-weight:bold">CREATE USER</font>:
	- Se utiliza para crear usuarios.
		- <font style="color:green">Ejemplo</font>:
			- `CREATE USER 'nombre_usuario'@'localhost' IDENTIFIED BY 'contraseña_usuario';`
				- @'localhost' indica que el usuario solo podrá acceder desde el mismo equipo donde se encuentra la base de datos.
					- 'localhost' se puede cambiar por la IP o el nombre del host si queremos que el usuario acceda desde otros equipo en la red.
# 5. Formas de trabajar con SQL
## <font style="color:salmon">5.1 Modo interactivo</font>
- Desde un terminal.
![[b853d33b-f92f-4088-9c1e-8f93f5ab54e3.webp]]
## <font style="color:salmon">5.2 Desde un programa</font>
![[6226e3e2-9616-4b72-a540-2d4346dd2b4a.webp]]
# 6. Entorno de trabajo
![[9017be0f-7fe2-419f-872d-9526e92aed62.webp]]
## <font style="color:salmon">6.2 Arquitectura servidora de archivos</font>
- Una aplicación que se ejecuta en una computadora personal puede acceder de forma transparente a los datos localizados en un servidor de archivos.
![[74c5ef41-b668-4631-a0d4-81d1912ceba8.webp]]
## <font style="color:salmon">6.3 Arquitectura Cliente/Servidor</font>
- Los frontales o front-ends de bases de datos, se ejecutan en la computadora personal.
- El motor de soporte o back-end de la base de datos que almacena y gestiona los datos se ejecuta en el servidor.
- Procedimiento:
	1. La consulta viaja a través de la red hasta el servidor de base de datos como una petición SQL.
	2. El motor de base de datos del servidor proceso la petición y explora la base de datos, que también reside en el servidor.
	3. Cuando se calcula el resultado, el motor de la base de datos envía de vuelta, a través de la red, una única contentación a la petición inicial, y la aplicación frontal la muestra en la pantalla del PC.
![[cliente-servidor 1.jpg]]
# 7. Creación y eliminación de bases de datos
- <font style="color:#08F; font-weight:bold">CREATE DATABASE</font>
	- **Creación** de una base de datos.
	- <font style="color:green">Ejemplo</font>:
		- `CREATE DATABASE Concesionario`
- <font style="color:#08F; font-weight:bold">DROP DATABASE</font>
	- Eliminación de una base de datos.
	- <font style="color:green">Ejemplo</font>:
		- `DROP DATABASE Concesionario`
- <font style="color:#08F; font-weight:bold">SHOW DATABASES</font>
	- Ver bases de datos existentes.
# 8. Modificación de bases de datos
## <font style="color:salmon">8.1 Definición de tablas</font>
- <font style="color:#08F; font-weight:bold">CREATE TABLE</font>
	- El usuario que crea la tabla se convierte en propietario.
	- <font style="color:#08F; font-weight:bold">DEFINIR COLUMNAS</font>
		- <font style="color:orange; font-weight:bold">Sintaxis</font>:
			 `CREATE TABLE nombre_tabla (`
				`nombrecolumna     tipo_columna [restricciones]`
				`[,nombrecolumna ......]`
				`[,restricciones])`
			- Las **restricciones** establecen reglas de integridad:
				- UNIQUE
				- REFERENCES
				- NULL
				- DEFAULT
				- ...
			- <font style="color:green">Ejemplo</font>:
				`CREATE TABLE DEPARTAMENTOS (`
					`COD INTEGER PRIMARY KEY,`
					`NOMBRE VARCHAR(45) NOT NULL,`
					`DIR VARCHAR(45),`
					`CIUDAD VARCHAR(45),`
					`TLF VARCHAR(9));`
	- <font style="color:#08F; font-weight:bold">PRIMARY KEY</font>
		- Es la clausula que **especifica la columna o columnas que forman la clave primaria**.
	- <font style="color:#08F; font-weight:bold">FOREIGN KEY</font>
		- <font style="color:orange; font-weight:bold">Sintaxis</font>:
		![[55e1252a-aa75-486e-87a7-78e15ce2bcf4.webp]]
[Link con explicación restricciones FOREIGN KEY](https://www.w3schools.com/sql/sql_foreignkey.asp)
## <font style="color:salmon">8.3 Modificación de tablas</font>
- <font style="color:#08F; font-weight:bold">ALTER TABLE</font>
	- Permite:
	![[b8e36fb5-6418-4a9d-8f3e-9646ce91cc7d.webp]]
	- La sentencia ALTER TABLE nombre_tabla va seguida de dos posibles palabras reservadas:
		- **ADD**:
			- Permite añadir.
		- **DROP**
			- Permite eliminar.
		- <font style="color:green">Ejemplos</font>:
			- Añadir columna:
				- ALTER TABLE NombreTabla ADD COLUMN...
			- Eliminar columna;
				- DROP TABLE NombreTabla DROP COLUMN...
			- Añadir una restricción:
				- ALTER TABLE NombreTabla ADD CONSTRAINT...
			- Eliminar una restricción:
				- DROP TABLE NombreTabla DROP CONSTRAINT...
			- <font style="color:green">Ejemplo de creación de una tabla para añadir dos nuevos campos</font>
				`CREATE TABLE Coche(`
					`Matricula VARCHAR(7) PRIMARY KEY,`
					`Marca VARCHAR(15) NOT NULL);`
				`ALTER TABLE Coche`
				`ADD COLUMN Modelo VARCHAR(15),`
				`ADD COLUMN Precio DECIMAL(8,2);`
	- <font style="color:orange; font-weight:bold">Sintaxis</font>:
		- **Cambiar el nombre de la columna** matriculacion a año:
			- `ALTER TABLE coche CHANGE matriculacion año INTEGER`
		- **Eliminar columna**:
			 `ALTER TABLE NombreTabla`
			 `NombreTabla DROP COLUMN NombreColumna;`
		- **Modificar las claves** primaria y ajena:
			- **Añadir clave ajena sin nombre**, por lo que no se podría borrar sin borrar la tabla entera:
				`ALTER TABLE Pedidos`
				`ADD FOREIGN KEY (ID_Empleado) REFERENCES Empleado(ID);`
			- **Añadir clave ajena con nombre**, por lo que se podría eliminar en el futuro sin borrar la tabla entera:
				`ALTER TABLE Pedidos`
				`ADD CONSTRAINT FK_Empleado`
				`FOREING KEY (ID_Empleado) REFERENCES Empleado(ID);` 
		- **Eliminar clave ajena**:
			`Alter TABLE Pedidos`
			`DROP CONTRAINT FK_Empleado;`
		- **Añadir restricciones**:
			- **Clave primaria**:
				- Donde (CAM1, CAM2, ETC) son el conjunto de campos, separados por comas, que conforman la clave primaria.
					ALTER TABLE NombreTabla
					ADD CONSTRAINT PK_NOMBRETABLA PRIMARY KEY (CAM1, CAM2, ETC);
			- **Clave foránea**:
				- Donde ‘FK_NomTabla_NomRelac’ es un nombre que identificará la relación entre ambas tablas. Por otro lado, (cf1_fk, cf2_fk,…) son el conjunto de claves foráneas de la tabla que harán referencia una por una, y en el orden que aparecen, a las claves primarias (cp1, cp2,…) presentes en la tabla referenciada. ‘NombreTablaRef’.
					ALTER TABLE NombreTabla ADD
					CONSTRAINT FK_NomTabla_NomRelac FOREIGN KEY (CF1_FK, CF2_FK, …)
					REFERENCES NombreTablaRef (CP1, CP2, …);
			- **Restricciones Check**:
				- Donde CK_NomTabla_NomRestric es el nombre dado a la restricción, y Condición es una condición establecida sobre alguna de las columnas de la tabla.
					ALTER TABLE NombreTabla
					ADD CONSTRAINT CK_NomTabla_NomRestric CHECK Condición;
					- **Eliminar una restricción**:
						ADD CONSTRAINT CK_NomTabla_NomRestric CHECK Condición;
## <font style="color:salmon">8.4 Creación de índices</font>

# 9. Introducción de datos en la base de datos
## <font style="color:salmon">Filas</font>
La **fila** es la unidad de datos más pequeña que se puede introducir en una base de datos relacional.
### <font style="color:orange">3 maneras de introducir filas a una tabla</font>
- **Sentencia INSERT:**
	- Añade una fila a una tabla.
	- La claúsula **INTO** especifica la tabla que recibe la nueva fila.
	- La claúsula **VALUE** especifica los valores que tendrá la nueva fila.
	- <font style="color:green">Ejemplo</font>:
		`INSERT INTO coche (matricula, marca, modelo, año) VALUES ('1234BCD', 'Audi', 'A3', '2016');`
- **Inserción de todas las columnas:**
	- Para omitir las columnas de la sentencia INSERT.
	- No se recomienda esta opción.
	- <font style="color:green">Ejemplo</font>:
		`INSERT INTO coche VALUES ('4567FTG', 'Mercedes', 'Benz', '2017')`
- **Carga masiva:**
	- Es la capacidad de carga de datos dese un archivo a una tabla.
# 10. Supresión de datos de la base de datos.
## <font style="color:salmon">La sentencia DELETE</font>
- Elimina filas seleccionadas de datos de una única tabla.
- <font style="color:orange; font-weight:bold">Sintaxis</font>:
	La cláusula **FROM** especifica la tabla destino que contiene las filas. La cláusula **WHERE** especifica qué filas de la tabla van a ser suprimidas.
- <font style="color:green">Ejemplo</font>:
	DELETE FROM coche WHERE matricula='4567FTG'
	- Se elimina el registro que contiene matrícula con valor 4567FTG.
## <font style="color:salmon">Suprimir todas las filas</font>
- Se suprimen todas las filas si se omite WHERE de una sentencia DELETE.
- La tabla no se elimina y tampoco se elimina las columnas.
- Para eliminar la tabla se debe utilizar DROP TABLE
- <font style="color:green">Ejemplo</font>:
	DELETE FROM coches;
- TRUNCATE TABLE es otro modo de para eliminar los registros de una tabla, pero no permite usar WHERE para filtrar el borrado. Por lo que se utiliza para eliminar todos los registros de la tabla.
# 11. Modificación de datos de la base de datos.
## <font style="color:salmon">La sentencia UPDATE</font>
- Modifica los valores de una o más columnas en las filas seleccionadas de una tabla única.
- La cláusula WHERE selecciona las filas de la tabla a modificar.
- <font style="color:green">Ejemplo</font>:
	- Se quiere asignar el año de matriculación 2018 a los coches de la marca Audi:
	UPDATE COCHE SET año = 2018 WHERE marca = 'Audi';
	- Para cambiar el año de matriculación de todos los coches:
	
	UPDATE COCHE SET año = 2018;
# Resumen
![[Pasted image 20250122182718.png]]
