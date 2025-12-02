# Etiqueta `<audio>`
- Se trata de una etiqueta usada en HTML5 que permite insertar audio.
- Se puede insertar un mensaje que se puede mostrar en caso de que el navegador no soporte la etiqueta `<audio>`:
```html
<audio src="pista.mp3" controls>
El navegador no soporta la etiqueta audio de HTML5
</audio>
```
## Atributos de la etiqueta `<audio>`
<font style="color:#08f; font-weight:bold">src</font>:
```html
<!-- Indica la fuente del archivo de audio, puede ser un valor URL -->
<audio src="pista.mp3"></audio>
```
<font style="color:#08f; font-weight:bold">autoplay</font>:
```html
<!-- La música suena de forma automática -->
<audio src="pista.mp3" autoplay></audio>
```
<font style="color:#08f; font-weight:bold">controls</font>:
```html
<!-- Mostrar los controles de reproducción de audio -->
<audio src="pista.mp3" controls></audio>
```
<font style="color:#08f; font-weight:bold">loop</font>:
```html
<!-- Reproducción en bucle -->
<audio src="pista.mp3" loop></audio>
```
<font style="color:#08f; font-weight:bold">muted</font>:
```html
<!-- Silencia el audio -->
<audio src="pista.mp3" muted></audio>
```
<font style="color:#08f; font-weight:bold">preload</font>:
```html
<!-- auto: el audio es cargado junto con la página -->
<audio src="pista.mp3" preload="auto"></audio>

<!-- metadata: solo se cargan los metadatos -->
<audio src="pista.mp3" preload="metadata"></audio>

<!-- none: el nose carga con la página, solo al final -->
<audio src="pista.mp3" preload="none"></audio>
```
