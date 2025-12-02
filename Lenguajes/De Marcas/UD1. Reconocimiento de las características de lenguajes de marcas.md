# 1. Clasificación
- Los más extendidos son HTML y XML.
- HTML es un lenguaje de marcas orientado a la creación de páginas web.
![[Pasted image 20241009124322.png]]
## <font style = "color:salmon">HTML</font>
- Lenguaje muy extendido, que tiene por objetivo ofrecer un lenguaje para diseño de páginas web que puedan ser interpretadas por un navegador
- Elementos de maquetación como CSS.
## <font style = "color:salmon">XML</font>
- Lenguaje de intercambio de información.
- Lenguaje de propósito general.
## <font style = "color:salmon">XHTML</font>
- Se suele definir como la versión XML de HTML.
## <font style = "color:salmon">JASON</font>
- Inicialmente era el formato de texto con el que JavaScript representaba en sus documentos los objetos.
- Actualmente es una alternativa de XML.
# 2. Características y ámbitos de aplicación
## <font style = "color:salmon">Características generales</font>
![[Pasted image 20241009125230.png]]
## <font style = "color:salmon">Características específicas</font>
- Los lenguajes tienen características concretas que no comparten con otros lenguajes.
	- Como la forma de etiquetar.
	- Los atributos de un elemento.
	- Etc.
## <font style = "color:salmon">Características y ámbitos de aplicación</font>
- HTML y XHTML:
	- Creación de paginas web.
- RSS:
	- Difusión de páginas web.
- MathML y OpenMath:
	- Notaciones matemáticas.
- TeX:
	- Ecuaciones matemáticas complejas.
- DocBook:
	- Generación de documentos separando del mismo la estructura lógica.
- Geography ML:
	- Modelaje, transporte y almacenamiento de información geográfica.
- SMIL:
	- Integración de audio, video, imágenes y cualquier contenido multimedia.
- VoiceXML:
	- Capacidad de intercambio de información con reconocimiento de voz.
- MusicXML:
	- Intercambio de partituras entre editores de partituras.
- Spacecraft ML:
	- Aeronáutica.
- XMPP:
	- Mensajería instantánea.
- VRML/X3D, STEP:
	- Gráficos 3D.
# 3. Estructura
[Diferencia entre atributo, elemento y etiqueta](https://es.semrush.com/blog/lista-de-html-tags/)
![[Pasted image 20241009200120.png]]
## <font style = "color:salmon">Estructura</font>
Las marcas o etiquetas son señales que se colocan entre el texto, añadiéndole significado:
![[Pasted image 20241009160322.png]]
## <font color="salmon">Etiquetas:</font>
- `<html>Todo documento html ha de estar delimitado entre estas etiquetas</html>`
	- `<!-- Los comentarios se declaran con esta entre estas etiquetas-->`
		- `<head>Aquí se colocan las etiquetas de índole informativo</head>`
			- `<title>Aquí se pondría el titulo del documento.</title>`
		- `<body>Estas etiquetas flanquean el cuerpo, que es donde está todo el contenido de la página</body>`
			- `<p>parafo</p>`
			- `<b>negrita</b>`
	- Las etiquetas pueden ser de 3 tipos:
		- De apertura: `<xxx>`
		- De cierre: `</xxx>`
		 Autocerradas: `<xxx/>`
- Ejemplo:
![[Pasted image 20241009160344.png]]
### <font style = "color:orange">Requerimientos</font>
- Algunas etiquetas tienen sus propios requerimientos.
	- Algunas necesitan aparecer cerradas, como `<a></a>`
	- Otras pueden tener etiquete de cierre o no , como `<p>`, que no siempre requiere `</p>`.
	- Otras como `<img>` , no llevan nunca etiqueta de cierre.
## <font style = "color:salmon">DOCTYPE</font>
Las declaraciones `<!DOCTYPE...>` son enlaces a documentos de definición, cuyo cometido es definir los elementos válidos del lenguaje y la relación entre ellos.
## <font style = "color:salmon">Atributos</font>
 - Los nombres de las etiquetas se escriben con minúsculas por convención.
	- Los elementos puedes tener una serie de propiedades denominados atributos.
		- Se declaran en la etiqueta de apertura, asignándoles un valor entre comillas (simples o dobles): atributo="valor"
		- Los atributos deben escribirse separados tanto de la etiqueta como de otros atributos.
			- `<font color = "orange">atributo de color</font>`
				- <font color = "orange">atributo de color</font>
			- `<font face = "fantasy">atributo de tipo de fuente</font>`
				- <font face = "fantasy">atributo de tipo de fuente</font>
			- `<font color = "orange" face = "fantasy">se pueden poner varios atributos</font>`
				- <font color = "orange" face = "fantasy">se pueden poner varios atributos</font>
		-  El principal atributo de `<html>` es lang, que identifica el idioma:
			- `<html lang="es">`

# 4. Herramientas de edición
- Cualquier sistema operativo cuenta con editores de texto que se pueden utilizar.
- No se requiere un entorno de desarrollo para crear documentos html.
# 5. Elaboración de documentos bien formados.
![[Pasted image 20241009195655.png]]
Los elementos pueden tener o no asignados uno o varios atributos.
El formato sería el siguiente:
`<Elemento atributol="valor1" atributo2="valor2" atributoN="valorN">`
# 6. Utilización de espacios en nombres
- `&nbsp;`
	- Se utiliza para poner más de un espacio en blanco se ha de utilizar el carácter especial 
![[Pasted image 20241010175009.png]]
![[Captura de Pantalla 2024-10-10 a las 17.50.40.png]]
- `<br>`
	- Se utiliza para conseguir un salto de línea.