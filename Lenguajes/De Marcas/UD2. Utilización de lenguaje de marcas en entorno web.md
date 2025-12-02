# 1. Estándares Web. Versiones. Clasificación.
## <font style = "color:orange">Estándares</font>
- Ejemplos:
	- <font style = "color:violet">W3C.</font>
	- WHATWG.
	- ECMA.
	- Khronos.
- Mas popular <font style = "color:violet">W3C.</font>:
	- Es un consorcio internacional de organizaciones relacionadas con las tecnologías de la información, y facilita la estandarización mediante la publicación de normas a seguir.
![[Pasted image 20241104180241.png]]
- Versiones y clasificación <font style = "color:violet">W3C:</font>
	- HTML:
		- Definir estructura documentos.
	- XML:
		- Utilizado en mayoría de tecnologías.
		- Permite trabajar en documentos de gran tamaño.
		- Soporta:
			- Bases de datos.
			- Comunicación entre aplicaciones.
			- Integración de información de manera efectiva.
	- CSS:
		- Hojas de estilo en cascada para asignar estilos en documentos.
	- JavaScript:
		- Para hacer las webs más dinámicas y funcionales.
# 2. Estructura de un documento HTML.
## <font style = "color:orange">Marcas o etiquetas</font>
- Se colocan entre el texto.
- Suelen ser un nombre encerrado entre signos de menor y mayor.
	- Ejemplos:
		- `<p>párrafo</p>`
		- `<b>negrita</b>`
- Un archivo HTML está compuesto por un conjunto de etiquetas, que se utilizan para definir la forma o estilo de cada parte del documento.
- El navegador se encarga de interpretar las etiquetas y mostrar el contenido con el formato definido por ellas.
## <font style = "color:orange">Partes de un documento HTML</font>
![[Pasted image 20241104182053.png]]
- <font style = "color:violet">DOCTYPE</font>
	- Enlace a documentos de definición para definir los elementos válidos del lenguaje y la relación entre ellos.
- <font style = "color:violet">HTML</font>
	- `<html></html>`: Etiquetas que delimitan el documento HTML.
- <font style = "color:violet">HEAD</font>
	- `<head></head>`: Etiquetas que delimitan la cabecera del documento.
	- Donde se colocan etiquetas de índole informativo, como el título de la página.
- <font style = "color:violet">BODY</font>
	- `<body></body>`: Etiquetas de delimitan el cuerpo del documento.
	- Es donde se coloca el contenido de la página.
# 3. Identificación de etiquetas  y atributos HTML
<font style ="color:salmon">Un archivo HTML es un conjunto de elementos</font>, cada uno con un nombre <font style = "color:violet">(etiquetas)</font>, un contenido y unas características <font style = "color:violet">(atributos)</font>. Las etiquetas delimitan el contenido de los elementos.
## <font style = "color:orange">3 tipos de etiquetas:</font>
- De apertura: `<xxx>`
- De cierre: `</xxx>`
- Autocerradas: `<xxx/>`
[Lista de etiquetas](https://carontestudio.com/blog/listado-de-etiquetas-html/)
## <font style = "color:orange">Sintaxis de un elemento</font>
`<nombre_elemento atributo1="valor1" atributo2="valor2" ...>`
	`contenido_elemento`
`</nombre_elemento>`
![[Pasted image 20241104191453.png]]
## <font style = "color:orange">Carácteres especiales</font>
Los más utilizados son:

| Carácter  | En números | En letras |
| --------- | ---------- | --------- |
| "         | `&#34;`    | `&quot;`  |
| <         | `&#60;`    | `&lt;`    |
| >         | `&#62;`    | `&gt;`    |
| &         | `&#38;`    | `&amp;`   |
| /         | `&#47;`    | `&frasl;` |
| ©         | `&#169;`   | `&copy;`  |
| §         | `&#167;`   | `&sect;`  |
| (espacio) | `&#160;`   | `&nbsp;`  |
# 4. Herramientas de diseño web
## <font style = "color:orange">WordPress</font>
- Sistema de gestión de contenido (CMS) gratuito y de código abierto.
- Se debe contar con alojamiento web.
- Se pueden ampliar sus funcionalidades con instalación de plugins.
## <font style = "color:orange">WIX</font>
- Herramienta de diseño web con versión gratuita y de pago.
- De fácil manejo.
- Con 3 niveles en función del tipo de usuario:
	- Editor Wix: Con opción de arrastrar y soltar.
	- Wix ADI (Inteligencia de Diseño Artificial): Creador automático de sitios web.
	- Velo by Wix: Plataforma para desarrolladores web independientes.
## <font style = "color:orange">Adobe Dreamweaver</font>
- Propiedad de Adobe.
- Cuenta con un editor muy efectivo de código.
- Los planes tienen precios elevados.
# 5. Hoja de estilo (CSS)
[Introducción a CSS](https://uniwebsidad.com/libros/css?from=librosweb)
[CSS Reference](https://www.w3schools.com/cssref/index.php)
## <font style = "color:orange">Regla CSS</font>
![[Pasted image 20241104233729.png]]
- <font style = "color:violet">Selector</font>:
	- Elemento o elementos HTML a los que se aplica la regla CSS.
- <font style = "color:violet">Declaración</font>:
	- Especifica los estilos que se aplican a los elementos.
	- <font style = "color:violet">Propiedad</font>:
		- Permite modificar una determinada característica del elemento.
	- <font style = "color:violet">Valor</font>:
		- Indica el valor que se le quiere dar a esa característica del elemento.
- <font style = "color:green">Ejemplo</font>:
	- p{color:blue}
## <font style = "color:orange">Comentarios CSS</font>
`/* Este es un comentario CSS */`
## <font style = "color:orange">Alcance aplicación reglas CSS</font>
- Sitio web completo.
- Un único documento HTML.
- Una porción del documento.
- Una etiqueta concreta.
## <font style = "color:orange">Control de aspectos gráficos CSS</font>
- Definir la distancia entre líneas del documento.
- Aplicar sangrado a las primeras líneas del párrafo.
- Colocar elementos en la página con mayor preción.
- Definir la visibilidad de los elementos.
## <font style = "color:orange">Unidades de medida CSS</font>
- En HTML solo se permiten los píxeles y los porcentajes.
- En CSS se permiten:
	- Píxeles (px) y porcentaje (%), al igual que antes.
	- Pulgadas (in)
	- Puntos (pt)
	- Centímetros (cm)
	- Otras unidades relativas, como se verá posteriormente.
## <font style = "color:orange">1. Estilos en línea</font>
- Cuando se utiliza el atributo style directamente en las etiquetas HTML.

| Ejemplo                                           |
| ------------------------------------------------- |
| &#60;p style= "color:green; font-size: 18px"&#62; |
## <font style = "color:orange">2. Hoja de estilos interna</font>
- Cuando los estilos individuales se agrupan en la cabecera del documento.
- Se debe utilizar selectores.
	- Ejemplo:
	-    `<style>`
			`p{color: blue;}`
		`</style>`
## <font style = "color:orange">3. Hoja de estilos externa</font>
- Consiste en definir las mismas reglas de una hoja de estilos interna en un archivo independiente.
- No se puede incluir contenido HTML.
- Se debe referenciar el archivo .css en el documento HTML:
	- `<link rel="stylesheet" type="text/css" href="nombre_hoja_estilos.css">`
## <font style = "color:orange">Herencia</font>
- Las propiedades de estilo definidas para una etiqueta son heredadas por el resto de las etiquetas que aparezcan más abajo en la jerarquía, siempre que éstas no definan dicha propiedad nuevamente.
## <font style = "color:orange">Elementos en línea y bloques (span y div).</font>
- Los elementos en línea se comportan como un texto dentro de un párrafo.
- Los elementos en bloque tienden a ocupar todo el espacio dentro del elemento padre o contenedor.
- Los títulos y párrafos son elementos en bloque ya que al introducir uno de estos elementos se produce un salto de línea.
- Las imágenes son elementos en línea ya que no produce un salto de línea.
![[Pasted image 20241106224905.png]]
### <font style = "color:violet">Etiqueta span</font>:
- Se utiliza para agrupar elementos en línea y asignar estilos a un elemento.
![[Pasted image 20241106225257.png]]
### <font style = "color:violet">Etiqueta div</font>:
- Se utiliza para agrupar contenido o crear secciones.
![[Pasted image 20241106225556.png]]
![[Pasted image 20241106225615.png]]
#### <font style="color:salmon">Posicionamiento elementos div</font>
##### Propiedad <font style="color:#DAF7A6">position</font>
- <font style = "color:violet">Estático</font>:
	- Valor por defecto de los elementos HTML.
	- Se define con la propiedad `position:static`
	- <font style="color:green">Ejemplo</font> de 2 bloques posicionados de forma estática:
![[Captura de Pantalla 2024-11-07 a las 18.03.18.png]]
![[Captura de Pantalla 2024-11-07 a las 18.04.20.png]]
- <font style = "color:violet">Relativo</font>:
	- Los elementos se ajustan con respecto a su posición normal.
	- Se define con la propiedad `position:relative`
	- <font style="color:green">Ejemplo</font> de 1 bloque verde posicionado de forma relativa:
![[Captura de Pantalla 2024-11-07 a las 18.07.54.png]]
![[Captura de Pantalla 2024-11-07 a las 18.08.31.png]]
- <font style = "color:violet">Fijo</font>:
	- Se utiliza para posicionar un elemento de forma fija.
	- Se define con la propiedad `position:fixed`
![[Pasted image 20241107203153.png]]
![[Pasted image 20241107203223.png]]
##### Propiedad <font style="color:#DAF7A6">float</font>
- Los elementos flotantes se apilan a uno de los lados mientras haya espacio de ancho en la página.
- Cuando no queda espacio, los elementos se colocan debajo de los anteriores.
- Se define con la propiedad `float`
- <font style="color:green">Ejemplo</font> de 2 bloques posicionados con la propiedad float:
![[Pasted image 20241107203716.png]]
- Se puede forzar que los elementos dejen de forzar sobre los anteriores.
- Propiedad `clear`
![[Pasted image 20241107210143.png]]
## <font style = "color:orange">Selectores a utilizar.</font>
### 1. <font style = "color:violet">De tipo</font>:
- Regla:
	- etiqueta {declaraciones_reglas}
- <font style="color:green">Ejemplo</font>:
	- h1 {color:green}
### 2. <font style = "color:violet">Universal</font>:
- Se representa mediante asterisco *
- Afecta a todos los elementos HTML.
- Se sutiliza como parte de otros selectores compuestos.
- <font style="color:green">Ejemplo</font>:
	- * {color:green}
### 3. <font style = "color:violet">Multiple</font>:
- Se pueden utilizar varios selectores separados con comas.
- <font style="color:green">Ejemplo</font>:
	- h1, h2, h3 { font-family:arial; color:blue;}
### 4. <font style = "color:violet">Descendiente</font>:
- Se restringe la aplicación de la regla a los elementos que se encuentren tras la aplicación sucesiva de dichos selectores simples.
- <font style="color:green">Ejemplo</font>:
-  p b {color:blue};
	- En el ejemplo se indica que el texto que pertenezca a un párrafo y esté en negrita sea de color azul.
- Se puede utilizar un asterisco para sustituir otro selector.
- <font style="color:green">Ejemplo</font>:
![[Pasted image 20241108184639.png]]
![[Pasted image 20241108184711.png]]
### 5. <font style = "color:violet">De clase</font>:
- Las clases son atributos en el que se pueden crear definiciones de estilos.
- Creación de una clase:
	- .nombredelaclase {declaraciones_reglas}
- <font style="color:green">Ejemplo</font>:
![[Pasted image 20241108185939.png]]
- Invocación de la clase:
	- `<etiqueta class="nombredelaclase">`
- <font style="color:green">Ejemplo</font>:
![[Pasted image 20241108190117.png]]
- <font style="color:yellow">Resultado</font>:
![[Pasted image 20241108190236.png]]
### 6. <font style = "color:violet">De id</font>:
- Funciona de manera similar al selector de clase, pero **cada identificador solo puede pertenecer a un único elemento**.
- Creación de un id:
	- `#identificador {declaraciones_reglas}`
- <font style="color:green">Ejemplo</font>:
![[Pasted image 20241108194249.png]]
- Invocación del id:
	- `<etiqueta id="nombre_id>`
- <font style="color:green">Ejemplo</font>:
![[Captura de pantalla de 2024-11-08 19-44-18.png]]
- <font style="color:yellow">Resultado</font>:
![[Pasted image 20241108194644.png]]
## <font style = "color:orange">El modelo de cajas</font>
![[Pasted image 20241103151429.png]]
- <b><font style = "color:violet">Contenido</font></b>:
	- Aparece todo lo que contenga el elemento.
- Relleno o margen interno (<b><font style = "color:violet">padding</font></b>):
	- Espacio entre contenido y borde.
- Borde (<b><font style = "color:violet">border</font></b>):
	- El borde que enmarca el elemento.
- Margen (<b><font style = "color:violet">margin</font></b>):
	- El espacio que se mantendrá entre el borde y otra caja adyacente.
- <font style="color:green">Ejemplo</font>:
![[Pasted image 20241108213913.png]]
- <font style="color:yellow">Resultado</font>:
![[ModeloCajas.png]]
## <font style = "color:orange">Unidades de medida</font>
- Pueden clasificarse en 2 grandes grupos:
	- <b><font style = "color:violet">Absolutas</font></b>.
	- <b><font style = "color:violet">Relativas</font></b>.
### <font style = "color:salmon">Absolutas</font>
- Se expresan en unidades.
- No se ven afectadas por las medidas de otros elementos.
	- <font style = "color:aqua">cm</font>: centímetros.
	- <font style = "color:aqua">mm</font>: milímetros.
	- <font style = "color:aqua">in</font>: pulgadas (= 2.54cm).
	- <font style = "color:aqua">px</font>: píxeles. Aunque se considere como unidad absoluta, depende de la resolución del dispositivo utilizado ya que, en ocasiones, un píxel puede estar formado por varios píxeles reales del dispositivo.
	- <font style = "color:aqua">pt</font>: puntos (1/72 pulgadas).
	- <font style = "color:aqua">pc</font>: picas (12 puntos).
### <font style = "color:salmon">Relativas</font>
- Las medidas cambian en relación con las de otros elementos.
- Se aconseja su uso para conseguir un diseño adaptable.
	%: porcentaje relativo al tamaño del elemento padre.
	- <font style = "color:aqua">em</font>: medida relativa al tamaño de la fuente del elemento. Por ejemplo, 2em indicaría un tamaño doble que el de la fuente.
	- <font style = "color:aqua">rem</font>: relativo al tamaño de la fuente del elemento raíz.
	- <font style = "color:aqua">ex</font>: es similar a em, pero tomando como referencia el tamaño de la letra x.
	- <font style = "color:aqua">ch</font>: relativa al ancho del dígito cero.
	- <font style = "color:aqua">vw</font>: relativo al 1% del ancho del área visible de la página (viewport).
	- <font style = "color:aqua">vh</font>: relativo al 1% de la altura del área visible de la página (viewport).
	- <font style = "color:aqua">vmin</font>: relativo al 1% de la menor de las dimensiones del viewport.
	- <font style = "color:aqua">vmax</font>: relativo al 1% de la mayor de las dimensiones del viewport.
#### <font style = "color:violet">Viewport</font>
- Es el área visible de la página web.
- Para usarlo hay que utilizar la etiqueta meta.
- Se puede ajustar:
	- width: Ancho.
	- height: Alto.
	- initial-scale: Escala.
	- minium-scale: Escala.
	- maximum-scale: Escala.
- <font style="color:green">Ejemplo</font>:
	- `<meta name="viewport" content="width=device-width, initial-scale=1.0">`
		- Se ajusta al ancho del dispositivo.
		- La escala se ajusta a 1, es decir, sin escalar.
## <font style = "color:orange">Atributos comunes de las hojas de estilos</font>
[[01. CSS-Atributos comunes]]
# 6. Validación de documentos HTML y CSS
1. Sintaxis.
2. Accesibilidad
3. SEO
4. Rendimiento
5. Usabilidad
- URL:
	- [MArkup Validation Service](https://validator.w3.org/)
# 7. Lenguaje de marcas para la sindicación de contenidos
Entre las funcionalidades que encontramos dentro de los lenguajes de marcas tenemos la sindicación de contenidos, tendrás que llevar a cabo una sindicación de contenidos de la página que estás desarrollando con las sentencias o instrucciones necesarias dentro del documento web y comprobar qué resultados se ofrecen a los distintos usuarios.

Al hablar de sindicación de contenidos con la utilización de lenguaje de marcas, debemos
comenzar por hablar de las RSS (Really Simple Sindication) como tecnología que se utiliza para la distribución de información de una web a los usuarios.

Habitualmente se requiere disponer de un software específico o lector de contenidos RSS, donde la información puede ser compartida mediante la suscripción a un servicio
de agregador de noticias, o bien, compartiendo la información existente en otros sitios web, haciendo la labor de emisor.

Entre la gran variedad de lectores de RSS (agregadores) distinguimos los siguientes tipos:
- De escritorio, instalables en el propio equipo del usuario.
- En línea, no requiere instalación, sólo el alta en el sitio web para su utilización.
- Plugins, extensiones de algunos navegadores como Opera o FireFox que permiten la suscripción a RSS

Esta técnica de distribuir contenidos web está derivada del lenguaje XML, permitiendo la construcción de archivos que almacenan el contenido a compartir, bien sea propio o mostrado en otras páginas web, dando lugar a la redifusión de contenidos web.

Ventajas
- Actualización de contenidos sin necesidad de intervención del usuario.
- Poco peso y facilidad de transmisión al tener un formato de texto plano.
- Posibilidad de filtrado de información sin necesidad de agrupación

<b><font style = "color:violet">Pasos a seguir en la creación de RSS</font></b>.
1. Creación de un canal de contenido

Va a requerir únicamente un editor XML y una página web, y algún tipo de herramienta como pueden ser Drupal o Joomla, que permiten la creación de una estructura y soporte para su creación y administración, con las ventajas de ser un software de código abierto, implementados en php con servidores apache y gestión de bases de datos a través de Mysql.

2. Validación de archivo RSS
W3C pone a nuestra disposición la herramienta de validación desde la url [https://validator.w3.org/feed/](https://validator.w3.org/feed/)

3. Publicación del archivo RSS
El siguiente paso es la subida del archivo a un servidor web, siguiendo unas sencillas pautas que consistirán en:
- Insertar en la página de inicio el enlace al archivo RSS.
- Habilitar el link que los lectores RSS seguirán para su lectura, suscribiéndose al feed.
- Envío de la dirección URI del archivo RSS al sitio web, donde se catalogan y almacenan los feeds para los distintos navegadores web.

<b><font style = "color:violet">Elementos principales de un RSS</font></b>

1. `<channel>`
Describe la fuente RSS e integra tres elementos obligatorios, `<tittle>` nombre del canal, `<link>` especifica el enlace al canal y `<description>` describe el contenido del canal.

Puede contener otra serie de elementos opcionales con los que definir las categorías de para el canal `<category>` o la dirección de la documentación del formato utilizado `<docs>`, entre otros.

2.  `<item>`
Son elementos que cuentan con la posibilidad de definir un determinado artículo RSS, pueden existir varios dentro del `<cannel>`, y contarán con elementos fundamentales como el elemento `<channel>`: Tittle, link y description. Además de opcionales como `<author>`, `<category>` o `<comments>`, por ejemplo.