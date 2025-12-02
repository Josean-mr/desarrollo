# Etiqueta `<video>`
La etiqueta `<video>`se utiliza para insertar vídeo en la página web.
**Sintaxis**:
```html
<video width="640" height="360" controls>
	<source src="ruta/al/video.mp4" type="video/mp4">
	<source src="ruta/al/video.ogv" type="video/ogg">
	<source src="ruta/al/video.webm" type="video/webm">
	Tu navegador no soporta la etiqueta de video HTML5.
</video>
```
**Explicación**:
1. Con la etiqueta `<video>`se inserta vídeo en la página web.
2. Con los atributos `width`y `height`se definen las dimensiones del vídeo.
3. Con el atributo `controls`se agregan controles de reproducción.
4. Con el atributo `source`indicamos la ruta del vídeo a insertar.
5. Se muestra el mensaje "Tu navegador no soporta la etiqueta de video HTML5." en caso de que no el navegador no soporte la etiqueta `<video>`.