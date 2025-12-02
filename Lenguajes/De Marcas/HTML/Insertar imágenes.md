# Etiqueta `<img>`
La etiqueta `<img>` permite introducir un imágenes en los documentos HTML. Requiere el atributo <font style="color:#08f; font-weight:bold">src</font> para indicar la dirección de la imagen.
**Sintaxis:**
```html
<img src="direccion\de\la\imagen"\>
```
## Otros atributos de la etiqueta `<img>`
<font style="color:#08f; font-weight:bold">alt</font>:
- Permite comentar las imágenes con texto.
<font style="color:#08f; font-weight:bold">width</font> y <font style="color:#08f; font-weight:bold">height</font>:
- Establecen el ancho y alto de la imagen.
<font style="color:green; font-weight:bold">Ejemplo</font>:
```html
<img src="https://images.pexels.com/photos/266706/pexels-photo-266706.jpeg" width="450px" height="300px"/>
```
<font style="color:#08f; font-weight:bold">border</font>:
- Se utiliza para aplicar bordes a la imagen.
- Los valores se expresan en píxel.
<font style="color:green; font-weight:bold">Ejemplo</font>:
```html
<img src="https://images.pexels.com/photos/266706/pexels-photo-266706.jpeg" border="5"/>
```
<font style="color:#08f; font-weight:bold">hspace</font> y <font style="color:#08f; font-weight:bold">vspace</font>:
- Permite establecer la distancia en píxeles entre la imagen y los objetos que se encuentran a los lados.
<font style="color:green; font-weight:bold">Ejemplo</font>:
```html
<!-- Establecer 20 pixeles de espacio a los lados y 30 pixeles de espacio arriba y abajo -->
<img src="https://images.pexels.com/photos/266706/pexels-photo-266706.jpeg" hspace="20" vspace="30"/>
```
- Equivalencia en <font style="color:salmon; font-weight:bold">CSS</font> es la propiedad <font style="color:#08f; font-weight:bold">margin</font>:
<font style="color:green; font-weight:bold">Ejemplo</font>:
```css
img {
	margin-left: 20px;
	margin-right: 20px;
	margin-top: 30px;
	margin-bottom: 30px;
}
```
- En <font style="color:salmon; font-weight:bold">CSS</font> se le puede asignar espacio entre elementos de un contendedor con la propiedad <font style="color:#08f; font-weight:bold">gap</font>:
```css
.galeria {
	display: flex; /* también se puede utilizar display: grid */
	gap: 15px;
	
	/* Opcional: Asignar espacio extra alrededor de todo el grupo */
	padding: 10px;
}
```
<font style="color:#08f; font-weight:bold">align</font>:
- Define la alineación de la imagen respecto al texto que se haya colocado antes o después de la misma.
<font style="color:green; font-weight:bold">Ejemplo</font>:
```html
<!-- Alinear la primera fila del texto con la parte superior de la imagen -->
<img src="https://images.pexels.com/photos/266706/pexels-photo-266706.jpeg" align="top" />
```
- Esté método esta obsoleto. Equivalencias en <font style="color:salmon; font-weight:bold">CSS</font>:

| Efecto deseado                     | Atributo HTML                 | Solución CSS                      |
| ---------------------------------- | ----------------------------- | --------------------------------- |
| Imagen a la izquierda, texto rodea | `<img align="left" />`        | `float: left;`                    |
| Imagen a la derecha, texto rodea   | `<img align= "right" />`      | `float: right;`                   |
| Imagen centrada                    | `<center><img... /></center>` | `display: block; margin: 0 auto;` |
| Alinear verticalmente con texto    | `<img align= "middle"/>`      | `vertical-align: middle;`         |
# Etiqueta picture
- Es una etiqueta que envuelve a otras etiquetas de imagen con el objetivo de que el navegador utilice la versión de la imagen que sea más adecuada en cada situación.
```html
<picture>
  <source media="(min-width: 1024px)" srcset="paisaje-grande.jpg">
  
  <source media="(min-width: 768px)" srcset="paisaje-mediano.jpg">
  
  <img src="paisaje-movil-cuadrado.jpg" alt="Paisaje de montañas" style="width: 100%;">
</picture>
```
- Explicación
1. El navegador lee el código de arriba a abajo.
2. Mide el ancho de la pantalla del usuario.
3. Si la pantalla tiene más de `1024px`, descarga `paisaje-grande.jpg` e ignora el resto.
4. Si no, verifica la siguiente condición (`768px`).
5. Si ninguna condición coincide, carga la imagen que está dentro de `<img>`.
## Uso de la etiqueta `<img>`con `srcses`
- Se utiliza la etiqueta `<img>`con `srcses`cuando la imagen es la misma, pero en diferentes tamaños.