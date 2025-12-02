# 1. Conceptos básicos
## <font style = "color:salmon">1.1 Sistemas de información</font>
Es un conjunto de actividades que administran la información relevante de una entidad, generalmente, una empresa.
- Se encarga de:
	- La distribución de los datos según unos determinados requerimientos.
	- La correcta compartición de la información entre usuarios.
	- Su almacenamiento en soportes adecuados basados en ordenadores y en los avances de las telecomunicaciones.
### <font style = "color:orange">Unidades de representación de información</font>
- bit:
	- 2 valores: 0 y 1
- byte:
	- Un grupo de 8 bits
- Campo:
	- Es cada dato al que puede hacerse referencia en un sistema de información.
	- Formado por un grupo de bytes.
- Registro:
	- Agrupación de datos que forman parte de una entidad común.
	- Un registro equivale a una fila de la table.
- Archivo:
	- Formado por registros del mismo tipo.
- Base de datos:
	- Conjunto de archivos que representa la información de un sistema.

![[Pasted image 20240922201543.png]]
## <font style = "color:salmon">1.2 Estructura básica de almacenamiento: el archivo</font>
- Es una estructura de datos de alto nivel.
- Los archivos se almacenan en registros de tipo lógico llamados registros.
- Los registros son estructuras de datos llamados campos.
### <font style = "color:orange">Ejemplo:</font>
- Nombre del archivo: CLIENTES.
- Nombre del registro: R_CLIENTES.
- Campo clave: NIF.
- Formato del registro:
![[Pasted image 20240922205105.png]]
### <font style = "color:orange">Ejemplo del contenido del archivo:</font>
![[Pasted image 20240922205141.png]]
### <font style = "color:orange">Características mas importantes de los archivos</font>
- Residen en soportes externos (DD), por lo que su existencia no está limitada al tiempo de ejecución que lo crea, sino que permanece cuando éste termina.
- Los datos pueden transportarse de un equipo a otro.
- Tiene capacidad de almacenamiento ilimitada ya que, aunque un soporte dispone de capacidad limitada, un archivo puede distribuirse en varios soportes.
### <font style = "color:orange">Clasificación de los archivos atendiendo a la función que realizan:</font>
![[Pasted image 20240922205725.png]]
- <font style = "color:#c2baf7">Permanentes:</font>
	- También conocidos con el nombre de **archivos maestros**.
	- Varían poco con el tiempo.
	- Se distinguen 3 tipos:
		- <font style = "color:#c9e4af">Constantes:</font>
			- Información prácticamente invariada.
			- Se utilizan como archivos de consulta.
		- <font style = "color:#c9e4af">De situación:</font>
			- Reflejan el estado actual de una empresa o entidad.
			- Se actualizan periódicamente para adaptarlos a una nueva situación.
		- <font style = "color:#c9e4af">Históricos:</font>
			- Se obtiene de los anteriores cuando se dejan de utilizar.
			- Se utilizan para estudios estadísticos o de consulta.
- <font style = "color:#c2baf7">De movimiento</font>:
	- En ellos se almacena temporalmente la información que se utiliza para actualizar los archivos de <font style = "color:#c9e4af">situación:</font>.
- <font style = "color:#c2baf7">De maniobra</font>
	- Archivos temporales creados durante la ejecución de un programa y borrados habitualmente al terminar el mismo.
	- Por ejemplo, archivos intermedios utilizados en procesos de ordenación.
### <font style = "color:orange">Operaciones sobre un archivo</font>
![[Pasted image 20240922205829.png]]
#### <font style = "color:green">Operaciones sobre un archivo</font>
- **Create**:
	- Crear estructura del archivo, establece la estructura y posición del archivo en el dispositivo de almacenamiento.
- **Open**:
	- Abrir el archivo creado para poder utilizarlo.
- **Read**:
	- Leer un registro de un archivo.
- **Write**:
	- Escribir un registro de un archivo.
- **Close**:
	- Cerrar un archivo cuando no se va a utilizar. Operación obligatoria antes de concluir un programa para evitar el riesgo de pérdida de información. Actualiza la situación real del archivo y elimina de memoria la tabla.
- **Rename**:
	- Renombrar archivo.
- **Delete**:
	- Eliminar un archivo.
- **Copy**:
	- Copiar un archivo.
- **Edit**:
	- Editar un archivo.
- **Indexar un archivo**:
	- Operación de alto nivel que permite dar a un archivo organización indexada.
# 2. Acceso a la información de los registros
## <font style = "color:salmon">3 modos de acceso</font>
- Acceso secuencial:
	- Las operaciones de lectura o de escritura se hacen sobre el registro físicamente contiguo al último que se utilizó.
- Acceso directo:
	- Los registros pueden leerse y escribirse directamente en la posición física que ocupan en el archivo (tambores y discos magnéticos).
- Acceso por índice:
	- Índice ordenado con las claves del archivo.
	- Para acceder a los registros, se busca secuencialmente la clave en el índice.
# 3. Gestión de archivos en soportes
## <font style = "color:salmon">2 tipos de soporte</font>
- Secuenciales:
	- Los datos se graban unos a continuación de otros.
	- Ejemplo:
		- Cinta magnética.
		![[Pasted image 20240923183837.png]]
- Direccionables:
	- Es espacio se divide en espacios direccionables individualmente.
	- Se accede a un dato por la dirección en que está almacenado.
	- Ejemplos:
		- CD-ROM
		- DVD
		![[Pasted image 20240923184217.png]]
## <font style = "color:salmon">Formas de asignación de bloques</font>
- El disco se divide en unidades mínimas llamadas clúster o bloques.
- 3 formas de asignar bloques:
	- <font style = "color:salmon">Asignación contigua</font>:
		- Requiere que los bloques de un archivo ocupen posiciones contiguas.
		- Acceso secuencial sencillo.
		- Fragmentación externa:
			- Es un problema que se produce cuando hay bloques suficientes para almacenar un archivo, pero este o ocupen posiciones contiguas.
	- <font style = "color:salmon">Asignación enlazada</font>:
		- Fragmenta el archivo en bloques que pueden estar distribuidos de forma aleatoria en el disco.
		- Funcionamiento:
			- El sistema operativo guarda la dirección del primer bloque.
			- Cada bloque almacena en sus últimos bytes la dirección del siguiente bloque.
			![[Pasted image 20240923185511.png]]
	- <font style = "color:salmon">Asignación indexada</font>:
		- Consiste en reunir todos los punteros en un bloque llamado índice.
		![[Pasted image 20240923185636.png]]
# 4. Ficheros planos
Las bases de datos y los archivos planos son dos enfoques diferentes para almacenar y gestionar datos. Cada uno tiene sus ventajas y desventajas, y la elección entre ambos depende de las necesidades y requisitos específicos de una aplicación o sistema.
## <font style = "color:salmon">Principales características de los ficheros planos</font>
- <font style = "color:salmon">1. Definición</font>
	- También conocidos como archivos de texto.
	- La información es legible.
	- Texto sin formato o CSV.
	- Cada registro o línea contiene una sola entidad o conjunto de datos relacionados.
- <font style = "color:salmon">2. Estructura:</font>
	- Estructura simple.
	- Búsqueda y acceso a datos más lentos y menos eficientes.
- <font style = "color:salmon">3. Facilidad de uso:</font>
	- Son fáciles de crear y editar.
	- Se pueden abrir con editor de texto.
	-  Es complicado mantener la integridad y la coherencia medida que crece la cantidad de datos.
- <font style = "color:salmon">4. Escalabilidad:</font>
	- A medida que crecen los datos, la gestión y el mantenimiento se vuelven más complejos y pueden llevar a problemas de rendimiento y organización.
- <font style = "color:salmon">5. Integridad de los datos:</font>
	- No proporcionan mecanismos para garantizar la integridad de los datos.
- <font style = "color:salmon">6. Ejemplo:</font>
	- Los archivos planos son comunes en escenarios simples.
### <font style = "color:salmon">En resumen</font>
En resumen, los archivos planos son útiles para situaciones sencillas y pequeñas cantidades de datos, mientras que las bases de datos son la elección preferida para aplicaciones complejas que requieren un almacenamiento y gestión eficiente de grandes volúmenes de información, manteniendo la integridad y escalabilidad necesarias.
# 5. Sistemas gestores de bases de datos (S.G.B.D)
## <font style = "color:salmon">¿Qué es una base de datos?</font>
Una base de datos es un conjunto de datos almacenados de forma organizada y estructurada en un soporte de información que es manejado por un ordenador.
### <font style = "color:orange">Componentes más importantes de una base de datos</font>
![[Pasted image 20240923192443.png]]
## <font style = "color:salmon">¿Qué es un sistema gestor de base de datos?</font>
Es un conjunto de programas que permiten la administración y gestión de la información de una base de datos.
![[Pasted image 20240923192806.png]]
- Los programadores y usuarios no tiene que saber cómo está distribuida y organizada la información. De ello se encarga el gestor de la base de datos.
- Proporciona diferentes niveles de abstracción.
- Conecta e implementa los distintos niveles de la arquitectura de la base de datos.
- Se encarga de transformar los datos requeridos por los programas de aplicación en registros físicos a leer, hacer la petición del sistema operativo y transferirla al área de trabajo del programa que la solicitó.
### <font style = "color:orange">Principales funciones del administrador:</font>
- Definir el esquema conceptual con el lenguaje de definición del SGBD.
- Controlar el acceso a la base de datos, concediendo permisos a los usuarios.
- Definir estrategias de recuperación frente a posibles fallos.
## <font style = "color:salmon">Objetivos base de datos</font>
![[Pasted image 20240923195341.png]]
- <font style = "color:salmon">1. Independizar los datos:</font>
	- Independizar los datos de las aplicaciones. Es lo que se denomina como independencia física e independencia lógica.
- <font style = "color:salmon">2. Redundancia mínima:</font>
	- Que los datos repetidos sean los mínimos posibles.
- <font style = "color:salmon">3. Seguimiento de las operaciones:</font>
	- Mecanismos de seguimiento de las operaciones como conexión de los usuarios, operaciones realizadas, etc.
- <font style = "color:salmon">4. Búsqueda versátil:</font>
	- Proporcionar versatilidad en las posibilidades de búsqueda de información facilitando al usuario varios criterios.
- <font style = "color:salmon">5. Protección de datos:</font>
	- Proteger los datos contra accesos no autorizados.
- <font style = "color:salmon">6. Integridad de la información:</font>
	- Controlar la integridad de la información de la base de datos. Para ello se debe dar respuesta ante:
		- Fallos de hardware.
		- Defectos en el código de los programas de aplicación.
		- Actualizaciones incompletas.
		- Inserción de datos incorrectos o no válidos.
		- etc.
- <font style = "color:salmon">7. Copias de seguridad:</font>
	- Mecanismos para realizar copias de seguridad de la información.
- <font style = "color:salmon">8. Solucionar problemas por concurrencia:</font>
	- Se puede dar el problema cuando varios usuarios intentan actualizar un registro determinado de la base de datos en el mismo instante de tiempo.
	- Se puede aplicar una técnica llamada cierre:
		- Es un semáforo que se pone en rojo cuando el registro está siendo actualizado. Las transacciones se ponen en cola.
## <font style = "color:salmon">Componentes</font>
El SGBD está dividido en 4 módulos:
- <font style = "color:salmon">Núcleo:</font>
	- Incorpora un conjunto de programas que coordinan y controlan el funcionamiento del SGBD.
	- Presentan las siguientes características:
	![[Pasted image 20240923201140.png]]
- <font style = "color:salmon">Lenguajes:</font>
	- Permiten la definición y el manejo de los datos de la base.
	- Ofrecen al administrador y a los usuarios 2 lenguajes:
		- Lenguaje de descripción de datos.
		- Lenguaje de manipulación de datos.
-  <font style = "color:salmon">Utilidades:</font>
	- Aplicaciones que facilitan el trabajo a los usuarios y programadores.
	- Tienen interfaz fácil de entender. Con menús que guían al usuario.
	![[Pasted image 20240923203052.png]]
- <font style = "color:salmon">Diccionario de datos:</font>
		- También conocido como catálogo del sistema.
		- Es un almacén integrado en el que se guarda toda la información referente a la descripción, gestión e implantación de la base de datos.
		- Están estructurados en tres capas o niveles:
			- Capa global:
				- Mayor nivel de abstracción.
				- Información común a todos los usuarios.
			- Capa intermedia:
				- Organiza la relación entre las capas globales y local.
			- Capa local:
				- Donde se representan los datos como grupos de información específica.
			![[Pasted image 20240923203644.png]]
# 6. Arquitectura ANSI-SPARC
Es una arquitectura de 3 niveles para los sistemas de bases de datos. Su objetivo es separar los programas de aplicación de la base de datos física.
![[Pasted image 20240924192306.png]]
## <font style = "color:salmon">2 tipos de independencia de datos</font>
- Independencia lógica:
	- Capacidad de modificar el esquema conceptual.
- Independencia física:
	- Capacidad de modificar el esquema interno.
## <font style = "color:salmon">3 niveles según la prespectiva desde la que sea vista la información</font>
![[Pasted image 20240924192830.png]]

- <font style = "color:salmon">Nivel interno:</font>
	- Se describe la **estructura física** de la base de datos mediante la definición del esquema interno.
	- El esquema interno especifica los detalles para el almacenamiento de la base datos y los métodos de acceso.
	- En el esquema interno se especifican:
		- Los archivos que contienen la información y su organización.
		- La forma de acceder a los registros.
		- El tipo y la longitud del registro.
- <font style = "color:salmon">Nivel conceptual:</font>
	- Está asociado al **esquema conceptual**.
	- En el esquema conceptual se definen los datos que intervendrán en el sistema.
	- Contiene los:
		- Los datos elementales (campos).
		- Los datos compuestos (registros).
		- Las relaciones entre campos elementales y compuestos.
		- Las reglas que rigen el funcionamiento de la empresa.
		- etc...
	- El esquema conceptual contiene:
		- Los registros.
		- Los campos.
		- Relaciones entre distintas entidades.
- <font style = "color:salmon">Nivel externo:</font>
	- Es el conjunto de **percepciones individuales** de la base de datos.
	- Cada visión individual se denomina subesquema o vista.
![[Pasted image 20240924193746.png]]
# 7. Modelos de las bases de datos
La manera en que la información se almacena en una base de datos da origen a un tipo y otro de base de datos.
![[Pasted image 20240924194106.png]]
## <font style = "color:salmon">Modelos basados en registros</font>
- Describen los datos a nivel conceptual y físicos.
- La base de datos está estructurada en registro de varios tipos.
![[Pasted image 20240924194458.png]]
<font style = "color:salmon">1. Modelo Jerárquico:</font>
- El primer modelo que se implementó.
- Utiliza estructura de árbol para la representación lógica de los datos.
- Un nodo tiene un único padre.
![[Pasted image 20240924194747.png]]
<font style = "color:salmon">2. Modelo de red:</font>
- Estructura de nodos conectados entre sí.
- Un nodo puede tener varios padres.
![[Pasted image 20240924195401.png]]
<font style = "color:salmon">3. Modelo relacional:</font>
- Formada por tablas que se caracterizan en:
	- No pueden contener campos repetidos.
	- No pueden existir registro duplicados, por lo que tiene un campo clave que identifica al registro y lo hace único.
![[Pasted image 20240924195718.png]]
## <font style = "color:salmon">Modelos orientados a objetos</font>
- Los sistemas de gestión de base de datos orientados a objetos (SGBDOO) son polivalentes.
- La arquitectura de los SGBDOO está basada en un enfoque cliente-servidor:
	- Objetos e identidad:
		- Cada entidad del mundo real es modelada a un objeto.
		- Cada objeto tiene un identificador único y está asociado a un estado que se represente por los valores de sus atributos y un comportamiento que se define por sus procedimientos llamados métodos que actúan sobre él.
	- Objetos complejos:
		- Los valores de los atributos de un objeto pueden ser objetos.
	- Encapsulamiento:
		- Cada objeto tiene definidos en su interior los métodos y la interfaz para tener acceso y capacidad de manipulación de dicho objeto.
	- Clases:
		- Todos los objetos definidos por los mismo atributos y métodos forman una clase.
		- Cada objeto que pertenece a una clase se dice instancia de clase.
	- Herencia:
		- Una clase (subclase) se puede definir como una especialización de otras clases (superclases) existentes, por lo que herederá sus atributos y métodos.
	- Sobrecarga:
		- Una operación puede tener asociados distintos métodos.
		- El sistema decide que método realiza la operación.
![[Pasted image 20240924204442.png]]
# 8. Bases de datos centralizadas
- Toda la información se encuentra en un solo lugar físico o lógico.
## <font style = "color:salmon">Características de las bases de datos centralizadas</font>
![[Pasted image 20240924204830.png]]
<font style = "color:salmon">1. Arquitectura monolítica:</font>
- Todo el sistema se encuentra en un único servidor o máquina.
- Puede generar un cuello de botella y limitar la escalabilidad.
<font style = "color:salmon">2. Control y seguridad centralizados:</font>
- Control y administración de la base de datos más simples.
- La base de datos es más vulnerable, ya que un fallo en el servidor centras puede provocar la pérdida de los datos.
<font style = "color:salmon">3. Mayor facilidad de mantenimiento:</font>
- Al tener una única ubicación, la administración, el respaldo y la aplicación de actualizaciones o parches son más fáciles de realizar, ya que solo es necesario intervenir en un servidor.
<font style = "color:salmon">4. Escalabilidad limitada:</font>
- El aumento de la carga de trabajo puede provocar un rendimiento deficiente.
<font style = "color:salmon">5. Latencia:</font>
- La ubicación centralizada puede generar latencia.
<font style = "color:salmon">6. Riesgo de pérdida de datos:</font>
- Mayor riesgo de pérdida de datos ante desastres naturales, ataques cibernéticos, etc.

Los sistemas tradicionales de administración de bases de datos (DBMS) como MySQL, PostgreSQL y Microsoft SQL Server, si se implementan en una única máquina, son ejemplos de bases de datos centralizadas.
### <font style = "color:orange">Ejemplos de bases de datos centralizadas:</font>
Sistemas tradicionales de bases de datos como MySQL que se implementan en una única máquina.
# 9. Bases de datos distribuidas
Una **Base de Datos Distribuida (BDD)** es una colección de datos distribuidos en diferentes nodos de una red de computadoras.
![[Pasted image 20240924205907.png]]
- Cada sitio de la red es autónomo.
## <font style = "color:salmon">Estrategias en el diseño de las BDD</font>
### <font style = "color:orange">Enfoque Top-Down</font>
- Empieza diseñando el esquema global.
- Luego se concibe la fragmentación de la base de datos.
- Se completa ejecutando, en cada sitio, el diseño físico de los datos.
### <font style = "color:orange">Enfoque Bottom-Up</font>
- Se basa en la integración de esquemas ya creados en un esquema global a partir de las bases de datos existentes.
## <font style = "color:salmon">Ventajas y Desventajas de los sistemas distribuidos</font>
### <font style = "color:orange">Ventajas</font>
- Acceso a los datos más rápido.
- Procesamiento más rápido porque varios nodos intervienen en el procesamiento.
- Pocas probabilidades de que una falla en un nodo afecte al sistema.
- Mayor tolerancia a fallos.
### <font style = "color:orange">Desventajas</font>
- Más complicado el control y manipulación de los datos.
- Complejo el aseguramiento de la integridad de la información.
- Control de concurrencia y mecanismos de control más complejos.
## <font style = "color:salmon">Sistema de Gestión de Base de Datos Distribuida</font>
Un **sistema de gestión de bases de datos distribuidas** (SGBDD) es un Sistema de Gestión de bases de datos que gestiona la base de datos distribuida.
### <font style = "color:orange">Funcionalidades adicionales de un SGBDD:</font>
- Accede a sitios remotos y trasmite consultas y datos a través de varios sitios mediante una red de comunicación.
- Almacena el esquema de distribución replicación de los datos en el catálogo del sistema.
- Establece las estrategias de ejecución de las consultas y las transacciones que acceden a los datos en más de un sitio.
- Decide sobre cual de los datos replicados acceder.
- Mantiene la consistencia de las copias de los datos replicados.
- Realiza la recuperación ante los fallos.
### <font style = "color:orange">Las BDD pueden ser:</font>
#### <font style = "color:salmon">Homogéneas</font>
- Todos los sitios tienen el mismo SGBD.
#### <font style = "color:salmon">Heterogéneas</font>
- Cada sitio puede tener un SGBD distinto.
### <font style = "color:orange">Problemas a resolver en las bases de datos distribuidas</font>
![[Pasted image 20240924230624.png]]
#### <font style = "color:salmon">Etapas de diseño</font>
<font style = "color:salmon">Fragmentación:</font>
- Decidir "como" se divide la base de datos y en "que" partes.
<font style = "color:salmon">Asignación:</font>
- Decidir "donde" se ubica cada parte, así como si se tiene replicación de datos.
## <font style = "color:salmon">Las 12 reglas de un SGBDD</font>
El principio fundamental  plantea que: "Desde el punto de vista del usuario, un sistema distribuido deberá ser idéntico a un sistema no distribuido".
![[Pasted image 20240924231209.png]]
# 10. Bases de datos no relacionales
## <font style = "color:salmon">Características:</font>
- Mas rápidas que las relacionales.
- Permiten almacenar grandes capacidades de información.
- Permiten almacenar diferentes tipos de información, lo que aporta gran flexibilidad.
- No hace uso del leguaje SQL tradicional.
- Ejemplos:
	- Cassandra.
	- Redis.
	- MongoDB
	- CouchDB
# 11. Big Data
## <font style = "color:salmon">Puede ser definido desde dos puntos de vista</font>
- Perspectiva del <font style = "color:salmon">tamaño de los datos</font>:
	- Conjunto de datos de gran volumen que supera la capacidad de procesamiento y almacenamiento de datos de las herramientas tradicionales.
	- La información, que se genera a partir de distintas fuentes puede ser:
		- Estructurada.
		- Semiestructurada.
		- No estructurada.
- Punto de vista <font style = "color:salmon">tecnológico</font>:
	- Conjunto de tecnologías y procesos que permiten recopilar y almacenar grandes cantidades de datos procedentes de distintas fuentes y de diferentes tipologías.
## <font style = "color:salmon">Las cinco Vs del Big Data</font>
![[Pasted image 20240926202716.png]]
<font style = "color:salmon">1. Volumen</font>
- Gran cantidad de datos generados y recopilados de distintos formatos y fuentes.
<font style = "color:salmon">2. Velocidad</font>
- El Big Data se genera y actualiza a gran velocidad.
<font style = "color:salmon">3. Variedad:</font>
- Los datos pueden ser estructurados, semiestructurados o no estructurados:
	- Estructurados: organizados como tablas de una base de datos.
	- Semiestructurados: cierto grado de estructuración, pero no siguen un esquema fijo. Ejemplo: XML o JSON
	- No estructurados: sin organización definida, como los correos electrónicos, vídeos, imagenes, etc.
<font style = "color:salmon">4. Veracidad:</font>
- A mayor información, más fácil será constatarla como veraz.
<font style = "color:salmon">5. Valor:</font>
- Proporciona valor ayudando a:
	- Optimizar procesos.
	- Conocer mejor a sus clientes.
	- Ofrecer publicidad acorde a sus gustos y demandas.
## <font style = "color:salmon">Analisis de datos</font>
Es el procesos de examinar, interpretar y extraer información significativa y valiosa de grandes conjuntos de datos.
### <font style = "color:orange">Principales técnicas del Análisis de datos</font>
<font style = "color:salmon">Análisis predictivo:</font>
- Basado en algoritmos y modelos estadísticos para predecir eventos futuros.
- Una de las técnicas mas conocidas es la Minería de Datos (Data Mining).
<font style = "color:salmon">Aprendizaje automático (Machine Learning):</font>
- Desarrollo de algoritmos y modelos capaces de aprender de datos para realizar predicciones y/o tomar decisiones sin una programación explícita.
<font style = "color:salmon">Minería de texto:</font>
- Enfocada en el análisis de datos no estructurados como:
	- Documentos.
	- Publicaciones en redes sociales.
	- Correos electronicos.
	- etc...
## <font style = "color:salmon">Inteligencia de Negocio</font>
También se conoce como Business Intelligence (BI), se refiere al conjunto de procesos, metodologías, herramientas y tecnologías utilizadas para transformar datos brutos en información significativa y fácil de interpretar.
![[Pasted image 20240929101944.png]]
# 12. Normativa legal sobre protección de datos.
## <font style = "color:salmon">Ley en rigor</font>
**Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales (LOPDGDD)**
[Link al BOE](https://www.boe.es/buscar/act.php?id=BOE-A-2018-16673)
### <font style = "color:orange">Aspectos clave de la ley</font>
![[Pasted image 20240929102724.png]]
<font style = "color:salmon">Ámbito de aplicación:</font>
- La ley aplica a cualquier tratamiento de datos personales en territorio español.
<font style = "color:salmon">Principio de protección de datos:</font>
- Establece los principios básicos que deben regir el tratamiento de los datos personales.
<font style = "color:salmon">Consentimiento:</font>
- Se establecen requisitos estrictos para obtener el consentimiento de los individuos cuyos datos se recopilan y procesan.
- El consentimiento debe ser libre, informada, específica e inequívoca.
<font style = "color:salmon">Derechos de los indviduos:</font>
- Derecho de las personas al acceso, rectificación, cancelación, limitación del tratamiento y portabilidad de los datos.
<font style = "color:salmon">Medidas de seguridad:</font>
-  Los responsables del tratamiento de datos deben implementar las medidas técnicas adecuadas para garantizar la seguridad de los datos y prevenir su pérdida.
<font style = "color:salmon">Transferencias internacionales:</font>
- Regula las transferencias de datos fuera de la UE.
<font style = "color:salmon">Registro de actividades de tratamiento:</font>
- Los responsables deben llevar a cabo un registro de las actividades de tratamiento que realizan.
<font style = "color:salmon">Autoridad de control:</font>
- La Agencia Española de Protección de Datos (AEPD) es la autoridad encargada de supervisar y hacer cumplir la ley en España.