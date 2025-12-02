# 1. Modelo entidad/relación.
Es una <font style="color:#f5d428; font-weight:500">representación gráfica y lingüística</font> de los objetos que forman parte del mundo real.
[Modelo Conceptual](https://www.youtube.com/watch?v=OfO5pPSPOa8)
## <font style="color:salmon">1.1 Elementos</font>
Para describir el esquema conceptual de la base de datos se debe construir su diagrama a través de una serie de <font style="color:#51a7fa"><strong>elementos</strong></font>.
### <font style="color:orange">1.1.1 Entidad</font>
- La <font style="color:#51a7fa"><strong>entidad</strong></font> es un objeto del mundo real.
- Suelen ser sustantivos.
- La representación gráfica es un <font style="color:#f5d428; font-weight:500">rectángulo</font> etiquetado:
	![[Entidad 1.png]]
- Se distinguen dos clases de entidad:
	- <font style="color:#51a7fa"><strong>Fuertes</strong></font>:
		- Son independientes.
		- Ejemplo:
			- <font style="color:#71bf41"><strong>Empleado</strong></font>.
	- <font style="color:#51a7fa"><strong>Débiles</strong></font>:
		- Su existencia está ligada a la existencia de otra entidad.
		- Ejemplo:
			- <font style="color:#71bf41"><strong>HijoEmpleado</strong></font>.
### <font style="color:orange">1.1.2 Atributo</font>
[Tu instituto online](https://www.tuinstitutoonline.com/cursos/baseavanzado1_v1606/03atributos.php)
- Un <font style="color:#51a7fa"><strong>atributo</strong></font> es una propiedad o característica asociada a una determinada entidad.
- La representación gráfica es una <font style="color:#f5d428; font-weight:500">elipse</font>:
	![[Atributos 1.png]]
-  <font style="color:#51a7fa"><strong>Dominio</strong></font>:
	- Es el conjunto de valores permitidos para un atributo.
	- Ejemplos:
		- <font style="color:#71bf41"><strong>Enteros</strong></font>
		- <font style="color:#71bf41"><strong>Cadena de texto</strong></font>
		- <font style="color:#71bf41"><strong>Fecha</strong></font>
		- ...
- <font style="color:#51a7fa"><strong>Atributo compuesto</strong></font>:
	- Cuando se pueden dividir en atributos independientes.
	-  Ejemplo:
		- Dirección se puede dividir en: <font style="color:#71bf41"><strong>calle</strong></font>, <font style="color:#71bf41"><strong>número</strong></font>,<font style="color:#71bf41"><strong> código Postal</strong></font>.
- <font style="color:#51a7fa"><strong>Atributo obiligatorio</strong></font>:
	- Si todas las concurrencias de atributo son valores no nulos y no vacíos.
- <font style="color:#51a7fa"><strong>Atributo opcional</strong></font>:
	- Si puede estar vacío o contener el valor nulo.
	-  Ejemplos:
		- <font style="color:#71bf41"><strong>SegundoApellido</strong></font>
		- <font style="color:#71bf41"><strong>TelefonoFijo</strong></font>
### <font style="color:orange">1.1.3 Clave</font>
- Es un <font style="color:#f5d428; font-weight:500">atributo que identifica unívocamente</font> cada una de las ocurrencias de ese tipo de entidad.
- Se suele subrayar la etiqueta del atributo que hace de clave.
	![[Clave 1.png]]
- El atributo o conjunto de atributos se denomina <font style="color:#71bf41; font-weight:500">identificador principal</font> y es la <font style="color:#71bf41; font-weight:500">clave primaria de la entidad</font>.
- Es preferible escoger una clave simple antes que una compuesta.
### <font style="color:orange">1.1.4 Relación</font>
- Una <font style="color:#71bf41; font-weight:500">relación</font> es una <font style="color:#f5d428; font-weight:500">asociación entre dos o más entidades</font>.
- Se suelen identificar por verbos.
- Se representa gráficamente por medio de un <font style="color:#f5d428; font-weight:500">rombo</font>:
	![[Relación 1.png]]
- Características:
	- <font style="color:#51a7fa; font-weight:500">Nombre</font>:
		- Deben tener un nombre.
	- <font style="color:#51a7fa; font-weight:500">Grado</font>:
		- Se refiere al número de entidades que participan.
			- 2 entidades: binarias.
			- 3 entidades: ternarias.
			- 4 entidades: cuaternarias.
			- ...
	- <font style="color:#51a7fa; font-weight:500">Cardinalidad</font>:
		- Número máximo de ocurrencias de cada tipo de entidad que pueden intervenir en una ocurrencia del tipo de relación.
### <font style="color:orange">1.1.5 Cardinalidad</font>
[Tutorial YouTube](https://youtu.be/7XnGypgLxvc?si=kCIT-KNJXkFzb3P8)
Hace referencia a la cantidad de elementos pertenecientes a una entidad que se pueden relacionar con otra cantidad determinada de elementos de otra entidad:
- <font style="color:#51a7fa; font-weight:500">(1:1) - Uno a uno</font> → Un elemento de una entidad se relaciona sólo con otro elemento de la otra entidad.
	![[Pasted image 20241113191425.png]]
- <font style="color:#51a7fa; font-weight:500">(1:M) o (1:N) - Uno a muchos</font> → Un elemento de una entidad se relaciona con varios elementos de la otra entidad.
	![[Pasted image 20241113191500.png]]
- <font style="color:#51a7fa; font-weight:500">(M:M) o (N:M)</font> - Muchos a muchos→ Son posibles todas las relaciones entre individuos pertenecientes a ambas entidades.
	![[Pasted image 20241113191522.png]]
### <font style="color:orange">1.1.6 Entidades débiles</font>
- Es cuando <font style="color:#f5d428; font-weight:500">toma su clave o claves principales de otras entidades</font>.
- La relación también es débil.
	- Ejemplo:
	![[Pasted image 20241113193250.png]]
	- <font style="color:#71bf41; font-weight:500">En este caso, la entidad E2 tomará la clave de E1</font>.
### <font style="color:orange">1.1.7 Generalización y Especialización</font>
- <font style="color:#51a7fa; font-weight:500">Generalización</font>:
	- <font style="color:#f5d428; font-weight:500">Es el resultado de la unión de dos o más conjuntos de entidades (de bajo nivel) para producir un conjunto de entidades de más alto nivel</font>.
	![[Pasted image 20241113194015.png]]
	- <font style="color:#51a7fa; font-weight:500">Especialización</font>:
		- Es lo contrario de de la generalización. <font style="color:#f5d428; font-weight:500">Es el resultado de tomar un subconjunto de entidades de alto nivel para formar un conjunto de entidades de más bajo nivel</font>.
[Enlace con ejemplo](https://sarreplec.caib.es/pluginfile.php/10828/mod_resource/content/2/72_generalizacin_y_especializacin.html)
![[BD03_CONT_R36_ejercicio_jerarquia.jpg]]
### <font style="color:orange">1.1.8 Agregación</font>
<font style="color:#f5d428; font-weight:500">Consiste en tratar una relación junto a las entidades con que se vincula como si todo el conjunto fuera una entidad</font>.
- Ejemplo:
	![[Pasted image 20241113203806.png]]
## <font style="color:salmon">1.2 Diagrama</font>
La entidad Empleado tiene como clave primaria el atributo RFC (se muestra subrayado);
para la entidad Artículo, su clave es el atributo Clave. Se observa que este diagrama
representa una relación binaria (de grado 2), ya que relaciona dos entidades. La cardinalidad de este ejemplo es de uno a muchos (1:M), ya que un empleado puede
vender varios artículos, pero un artículo solo puede ser vendido por un empleado. Si los
artículos pudiesen ser vendidos por varios empleados, esta relación sería del tipo muchos a muchos (M:M).
![[Pasted image 20241113204219.png]]
## <font style="color:salmon">1.3 Diagrama</font>
A la hora de crear un esquema conceptual utilizando el Modelo Entidad/Relación, se
debe intentar que el diagrama resultante cumpla los siguientes factores:
![[Pasted image 20241113204329.png]]
- <font style="color:#80a23a; font-weight:500">Completo</font>: En el modelo se reflejan todas las características de la realidad que pretende representar.
-  <font style="color:#33a9c9; font-weight:500">Correcto</font>: Utiliza correctamente todos los elementos necesarios del Modelo Entidad/Relación.
-  <font style="color:#75549e; font-weight:500">No Redundante</font>: No existen propiedades repetidas en el esquema.
-  <font style="color:#b73633; font-weight:500">Legible</font>: Que una persona que no ha participado en la elaboración del esquema sea capaz de comprenderlo.
- <font style="color:#f68928; font-weight:500">Extensible</font>: Se adapta a futuros cambios que no afecten totalmente a las estructuras del diagrama.
-  <font style="color:#c43b38; font-weight:500">Normalizado</font>: El esquema está en la forma normal de Boyce-Codd, esta propiedad puede posponerse hasta que el diagrama se transforme al modelo lógico de datos elegido (relacional, jerárquico o de redes).
# 2. Modelo relacional
En el <font style="color:#51a7fa; font-weight:500">Modelo Relacional</font> <font style="color:#f5d428; font-weight:500">los datos se estructuran lógicamente en forma de relaciones (tablas), siendo el objetivo fundamental del modelo mantener la independencia de la estructura lógica respecto de la estructura física</font>.
## <font style="color:salmon">2.1 Arquitectura</font>
<font style="color:#f5d428; font-weight:500">3 niveles</font>:
- <font style="color:#51a7fa; font-weight:500">Esquema conceptual</font>
	- <font style="color:#f68928; font-weight:500">Tablas</font>.
- <font style="color:#51a7fa; font-weight:500">Esquema externo</font>
	- <font style="color:#f68928; font-weight:500">Vistas</font>
- <font style="color:#51a7fa; font-weight:500">Esquema interno</font>
### <font style="color:orange">2.1.1 Tablas</font>
![[Pasted image 20241113213317.png]]
![[db-relacionterminos.jpg]]
- <font style="color:#51a7fa; font-weight:500">Tupla</font>:
	- Fila de la tabla que se corresponde con cada ocurrencia de la relación.
- <font style="color:#51a7fa; font-weight:500">Cardinalidad</font>:
	- Número de filas de la tabla.
- <font style="color:#51a7fa; font-weight:500">Grado</font>:
	- Número de atributos de la tabla.
- <font style="color:#51a7fa; font-weight:500">Clave</font>:
	- Atributo que se utiliza para identificar filas en una tabla.
	- Pueden ser clave foránea si es clave en otra tabla distinta.
- <font style="color:#51a7fa; font-weight:500">Dominio de un atributo</font>:
	- Conjunto de valores que puede tomar dicho atributo.
	- Pueden ser:
		- Generales.
		- Restringidos.
### <font style="color:orange">2.1.2 Vistas</font>
- Una <font style="color:#51a7fa; font-weight:500">vista</font> <font style="color:#f5d428; font-weight:500">es una tabla virtual que el usuario puede crear y manejar, y que no tiene que corresponderse con ningún archivo del nivel interno</font>.
- Las <font style="color:#51a7fa; font-weight:500">vistas</font> se utilizan para describir el <font style="color:#51a7fa; font-weight:500">esquema externo</font>.
## <font style="color:salmon">2.2 Reglas de integridad</font>
- La <font style="color:#51a7fa; font-weight:500">integridad</font> es un objetivo que se cumple si se consigue mantener la <font style="color:#f5d428; font-weight:500">coherencia y la veracidad de la información en la base de datos</font>.
- <font style="color:#f5d428; font-weight:500">Restricciones</font> principales que forman parte del Modelo Relacional que se deben cumplir <font style="color:#f5d428; font-weight:500">para mantener la base de datos relacional íntegra</font>:
	- <font style="color:#51a7fa; font-weight:500">Integridad de entidad</font>
	- <font style="color:#51a7fa; font-weight:500">Integridad de clave</font>
	- <font style="color:#51a7fa; font-weight:500">Integridad referencial</font>
### <font style="color:orange">2.2.1 Integridad de entidad</font>
- <font style="color:#f5d428; font-weight:500">Ningún valor de la clave primaria de una relación puede ser nulo o desconocido</font>.
### <font style="color:orange">2.2.2 Integridad de clave</font>
- Los valores de claves candidatas en una relación deben ser únicos para cada tupla.
### <font style="color:orange">2.2.3 Integridad referencial</font>
- <font style="color:#f5d428; font-weight:500">Afecta a la inserción, modificación y borrado de tuplas</font>.
- Para la <font style="color:#51a7fa; font-weight:500">inserción</font> y <font style="color:#51a7fa; font-weight:500">modificación</font>, el SGBD relacional debe asegurarse de que, al introducir un valor de una clave foránea, ese valor sea nulo o exista en todas las relaciones en las que la clave foránea
- Para la <font style="color:#51a7fa; font-weight:500">eliminación</font>, no se permite borrar una tupla de una relación cuyo valor de clave primaria exista como valor de la clave foránea de otra relación.
# 3. Paso del Modelo E/R a Modelo Relacional.
![[Pasted image 20241114194052.png]]
- Antes de pasar al <font style="color:#51a7fa; font-weight:500">Modelo Relacional</font>, se debe <font style="color:#f5d428; font-weight:500">comprobar que no existen elementos que no se puedan representar en el Modelo Relacional</font>.
## <font style="color:salmon">3.1 Eliminación de jerquías de generalización</font>
- <font style="color:#51a7fa; font-weight:500">Integrar todas las entidades en una única</font>:
	- La nueva entidad contendrá todos los atributos.
	- Inconvenientes:
		- Genera demasiados valores nulos en los atributos opcionales.
		- Ralentiza el proceso de búsqueda al tener en cuanta todas las tuplas.
- <font style="color:#51a7fa; font-weight:500">Considerar cada subentidad como entidad</font>:
	- Se añaden los atributos de la entidad genérica a la subentidad y la clave primaria genérica pasa a serlo de las nuevas entidades creadas.
	- Inconvenientes:
		- Se pierde el concepto de entidad genérica.
		- Los accesos a la entidad genérica deben convertirse en accesos a todas las subentidades.
		- Los atributos de la entidad genérica son repetidos en cada subentidad.
		- Sólo es válida para jerarquías totales y exclusivas.
		- Si la entidad genérica tiene alguna relación, ésta debe propagarse a cada subentidad.
## <font style="color:salmon">3.2 Eliminar los atributos compuestos</font>
- <font style="color:#f5d428; font-weight:500">El Modelo Relacional sólo permite representar atributos simples</font>, por lo que deben convertirse los atributos compuestos.
- Existen 2 alternativas:
	- Atributo FechaNacimiento compuesto de Día, Mes y Año convertirlo en DíaNacimiento, MesNacimiento y AñoNacimiento.
	- Considerar el atributo compuesto como simple.
## <font style="color:salmon">3.3 Eliminar atributos multivalor</font>
