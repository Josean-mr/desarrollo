# 1. Descripción de la información transmitida en documentos XML
## <font style = "color:orange">Componentes o nodos</font>:
- <font style="color:#08F; font-weight:bold">Raíz:</font>
	- El primer elemento que aparece en el documento designado con **"/"**.
- <font style="color:#08F; font-weight:bold">Elementos:</font>
	- Unidad básica del documento, donde se almacena la información a transmitir, con sus correspondientes etiquetas.
- <font style="color:#08F; font-weight:bold">Atributos:</font>
	- Asignan valores a los elementos.
- <font style="color:#08F; font-weight:bold">Texto:</font>
	- Grueso de la información dentro del documento.
- <font style="color:#08F; font-weight:bold">Comentarios:</font>
	- Con funcionalidad idéntica a HTML.
- <font style="color:#08F; font-weight:bold">Espacio de nombres:</font>
	- Permite diferenciar etiquetas.
- <font style="color:#08F; font-weight:bold">Instrucciones de procesamiento:</font>
	- Enviadas al procesador, comienzan con **`<?`** y finalizan con **`¿>`**
- <font style="color:#08F; font-weight:bold">Entidades predefinidas:</font>
	- Utilizadas para representar caracteres especiales de marcado.
- <font style="color:#08F; font-weight:bold">Secciones CDATA</font>:
	- Grupos de caracteres que requiere ser analizados por el procesador.
- <font style="color:#08F; font-weight:bold">DTD:</font>
	- Recoge las reglas que se aplican al documento DTD.
## Estructura, sintaxis y reglas
## <font style = "color:salmon">Estructura</font>:
<font style="color:green; font-weight:bold">Ejemplo:</font>
```xml
<?xml version="1.0" encoding="UTF-7" ?>
<album>
	<autor>Alejandro Sanz</autor>
		<titulo>Más Aniversario</titulo>
	<formato>MP3</formato>
		<localizacion>Varios CD2 </localizacion>
</album>
```
### <font style="color:salmon">Un documento XML puede contener:</font>
#### <font style="color:orange">1) Prólogo:</font>
- <font style="color:#08F; font-weight:bold">Declaración del documento.</font>
- <font style="color:#08F; font-weight:bold">Instrucciones para el procesado del documento.</font>
- <font style="color:#08F; font-weight:bold">Comentarios.</font>
- <font style="color:#08F; font-weight:bold">Indicación del esquema DTD, XSD o Relax NG.</font>
- <font style="color:#08F; font-weight:bold">Indicación de otros documentos que le afectan.</font>
#### <font style="color:orange">2) Ejemplar o elemento raíz:</font>
- <font style="color:#08F; font-weight:bold">Más elementos</font>, que pueden ser de diferentes tipos como: Padre, hermano, hijo o vacío.
- <font style="color:#08F; font-weight:bold">Atributos</font>, añaden información a los elementos que acompañan, irán dentro de etiquetas, separado del nombre por uno o más espacios.
- <font style="color:#08F; font-weight:bold">Entidades</font>, Tipo de marcado que identifica el nombre del archivo que queremos añadir al documento.
- <font style="color:#08F; font-weight:bold">Atributos</font>, añaden información a los elementos que acompañan. Irán dentro de las etiquetas, separado del nombre por uno o más espacios.
- <font style="color:#08F; font-weight:bold">Notaciones</font>, tipo de marcado que establece la aplicación que procesa el archivo.
- <font style="color:#08F; font-weight:bold">Texto normal</font>.
- <font style="color:#08F; font-weight:bold">Comentarios</font>
#### <font style="color:orange">Sintaxis</font>
<font style="color:#08F; font-weight:bold">Espacios en blanco</font>
**xml=space**
- Puede tomar los valores "preserve" o "default"
	<font style="color:green; font-weight:bold">Ejemplo:</font>
	```xml
	<?xml version="1.0"?>
	<refranes>
		<cita> Vísteme despacio que tengo prisa ?</cita>
	<popular xml:space="preserve">
		De los 40 para arriba,
		no te mojes la barriga
		</popular>
	</textos>
	```
<font style="color:#08F; font-weight:bold">Marcas</font>
- Partes que empiezan con "<" y acaban ">" .
	- <font style="color:green; font-weight:bold">Ejemplo:</font> <Día>
- En referencias de entidad, empiezan por "&" acaban con ";".
	- <font style="color:green; font-weight:bold">Ejemplo:</font> &quot; // Para representar comillas dobles
	![[Pasted image 20250218202920.png]]
# 2. Creación de descripciones de documentos, utilización de métodos de descripción de documentos XML.
![[5fb6170f-60b8-4cfe-9570-0e06e378b9bf.webp]]
### <font style="color:salmon">Declaración del tipo de elemento:</font>
- Dice el nombre del tipo que seguirá el documento XML, en forma de enlace que figura en su elemento raíz.
	- <font style="color:green; font-weight:bold">Ejemplo:</font>
	`<!DOCTYPE MARCAS_COCHES SYSTEM "marcasCoches.dtd">`
- Declaración:
	- `<!DOCTYPE`
- Nombre del tipo:
	- `MARCAS_COCHES`
- Archivo donde se ha almacenado el documento XML:
	- `"marcasCoches.dtd"`
#### <font style="color:orange">Los diferentes tipos de elementos son:</font>
![[Pasted image 20250218210349.png]]
### <font style="color:salmon">Declaración de listas de atributos:</font>
- Permiten definir el conjunto de atributos que va a tener cada elemento.
- Se deben declarar en cada elemento creado.
	- <font style="color:green; font-weight:bold">Sintaxis para un atributo:</font>
	`<!ATTLIST nombre_elemento nombre_atributo tipo_atributo declaración_por_defecto>`
	- <font style="color:green; font-weight:bold">Sintaxis para más de un atributo:</font>
	`<!ATTLIST nombre_elemento nombre_atributo tipo_atributo declaración_por_defecto nombre_elemento nombre_atributo tipo_atributo declaración_por_defecto>`
#### <font style="color:orange">Declaraciones de atributos:</font>
![[Pasted image 20250218214204.png]]
#### <font style="color:orange">Especificación de tipo de atributo:</font>
- **Se utiliza para limitar los valores que puede tomar el contenido del atributo.**
<font style="color:#08F; font-weight:bold">Cadena</font>:
- **CDATA**
- Admite valores de cadenas de caracteres.
- <font style="color:green; font-weight:bold">Ejemplo:</font>
	```XML
	<!ATTLIST VEHICULOS tipo CDTA #REQUIRED>
	```
<font style="color:#08F; font-weight:bold">Enumerado</font>:
- Se define una lista predeterminada de valores que permite el atributo.
- <font style="color:green; font-weight:bold">Ejemplo:</font>
	```XML
	<!ATTLIST VEHICULOS tipo (turismo, SUV, familiar) #IMPLIED>
	```
<font style="color:#08F; font-weight:bold">Asignación de ID</font>:
- **ID**
- Permite la identificación única de un elemento.
- No puede existir otro elemento con un atributo tipo ID dentro del documento XML.
- <font style="color:green; font-weight:bold">Ejemplo:</font>
	```XML
	<!ATTLIST VEHICULOS año ID #REQUIRED>
	```
	Se asigna el atributo año de tipo ID, al elemento VEHICULOS.
<font style="color:#08F; font-weight:bold">Inclusion de distintos tipos de objetos, como imágenes</font>:
- **ENTITY**
- **ENTITIES**
# 3. Asociación de descripciones con documentos. Validación.
## <font style = "color:salmon">DTD (Document Type Definition)</font>:
[XML y DTD con Ejemplos | Introducción al XML | XML Well Formed | DTDs - YouTube](https://youtu.be/3SoJklNsyfE?si=pNGAsbNhFgCBBdRf)
### <font style="color:#08F; font-weight:bold">DTD interna.</font>
- Las reglas van definidas en el propio documento XML.
- En la declaración debe incluirse el elemento tipo DOCTYPE.
- <font style="color:green; font-weight:bold">Ejemplo:</font>
	```xml
	<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE alumnos [
	<!ELEMENT alumnos (nuevos)*>
	<!ELEMENT nuevos (nombre, primerapellido, segundoapellido)>
	<!ELEMENT nombre (#PCDATA)>
	<!ELEMENT primerapellido (#PCDATA)>
	<!ELEMENT segundoapellido (#PCDATA)>
]>
<alumnos>
	<nuevos>
		<nombre>Juan</nombre>
		<primerapellido>Blanco</primerapellido>
		<segundoapellido>Peral</segundoapellido>
	</nuevos>
<alumnos>
	<nuevos>
		<nombre>Ana</nombre>
		<primerapellido>Vega</primerapellido>
		<segundoapellido>Luz</segundoapellido>
	</nuevos>
<alumnos>
	<nuevos>
		<nombre>Noelia</nombre>
		<primerapellido>Cano</primerapellido>
		<segundoapellido>Esera</segundoapellido>
	</nuevos>
</alumnos>
```
### <font style="color:#08F; font-weight:bold">DTD externa.</font>
- Los elementos se declaran fuera de un documento XML.
- Se accede al especificar los atributos del sistema que pueden consistir en un **archivo tipo .dtd** (DTD externa privada) o una **dirección URL** (DTD externa pública).
#### <font style="color:orange">DTD externa privada:</font>
- Con **archivo .dtd**.
- <font style="color:green; font-weight:bold">Ejemplo:</font>
```xml
	<!DOCTYPE elemento-raíz SYSTEM "URI">
	Y a modo de ejemplo tendríamos el siguiente código:
	<?xml version="1.0" encoding="UTF-8"?>
	<!DOCTYPE alumnos [
		<!ELEMENT alumnos (nuevos)*>
		<!ELEMENT nuevos (nombre, primerapellido, segundoapellido)>
		<!ELEMENT nombre (#PCDATA)>
		<!ELEMENT primerapellido (#PCDATA)>
		<!ELEMENT segundoapellido (#PCDATA)>
	]>
```
- Encontrando el siguiente documento XML válidol
	```xml
	<?xml version="1.0" encoding="UTF-8" standalone="no"?>
	<!DOCTYPE alumnos SYSTEM "alumnos.dtd">

	<alumnos>
		<nuevos>
			<nombre>Juan</nombre>
			<primerapellido>Blanco</primerapellido>
			<segundoapellido>Peral</segundoapellido>
		</nuevos>
	<alumnos>
		<nuevos>
			<nombre>Ana</nombre>
			<primerapellido>Vega</primerapellido>
			<segundoapellido>Luz</segundoapellido>
		</nuevos>
	<alumnos>
		<nuevos>
			<nombre>Noelia</nombre>
			<primerapellido>Cano</primerapellido>
			<segundoapellido>Esera</segundoapellido>
		</nuevos>
	</alumnos>
	```
#### <font style="color:orange">DTD externa pública:</font>
- Con **URL**.
	```XML
	<?xml version="1.0" standalone="no"?>
	<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
		"http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
	<html>
		<head>
			<title>Título</title>
		</head>
		<body>
			<p>Párrafo</p>
		</body>
	</html>
	```
# Herramientas de creación y validación.
- La validación de un documento XML es el proceso de verificar que un archivo XML cumple con una estructura y reglas predefinidas establecidas en un esquema o un **DTD** (Document Type Definition).
- Validación con:
	- DTD
	- XML Schema
### <font style="color:#08F; font-weight:bold">Editores de texto:</font>
- Notepad ++
- Visual Studio Code
### <font style="color:#08F; font-weight:bold">Navegadores web:</font>
- Edge.
### <font style="color:#08F; font-weight:bold">Editores web:</font>
- XML Editor
- XML Viewer
### <font style="color:#08F; font-weight:bold">Entornos de desarrollo integrado:</font>
- Eclipse.