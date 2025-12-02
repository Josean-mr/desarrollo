# Clases
- Una descripción de un conjunto de objetos que comparten los mismos atributos, operaciones, métodos y semántica.
## Notación de clase
- Las clases se representan por rectángulos que muestran el nombre de la clase y opcionalmente el nombre de las operaciones y atributos.
![[Pasted image 20250326181446.png]]
- Los **atributos** también son llamados **variables de instancia**.
- Los **métodos** u operaciones son la forma como interactúa el objeto con su entorno.
![[Pasted image 20250326181829.png]]
## Las relaciones entre clases pueden ser
- Asociativas.
- De herencia.
- De uso.
- De agregación.
### Cardinalidad de las relaciones.
- **Uno o muchos**: 1...* (1..n).
- **0 o muchos**: (0..n).
- **número fijo**: m (m denota el número).
### <font style="color:#08F">Herencia (Especialización/Generalización)</font>
- Una subclase hereda los métodos y atributos especificados por una superclase.
- Una subclase tendrá sus propios métodos y atributos y los heredados de la superclase que sean visibles (public y protected).
- Para que exista herencia clara, las subclases responden a la expresión "**es un**". Ejemplo: Camión "es un" vehículo.
![[Pasted image 20250326182616.png]]
### <font style="color:#08F">Agregación</font>
[Java Composicion y la reutilización del código]([Java Composicion y la reutilización del código - Arquitectura Java](https://www.arquitecturajava.com/java-composicion-y-la-reutilizacion-del-codigo/))
![[Pasted image 20250326194009.png]]
- Cuando se require componer objetos que son instancias de clases definidas, se presentan dos posibilidades:
	- **Por Valor:**
		- También se le llama relación de **Composición**.
		- Tipo de relación **estática**.
		- El **tiempo de vida del objeto está condicionado por el tiempo de vida que lo incluye**.
		- El Objeto base se construye a partir del objeto incluido, es decir, es "**parte/todo**".
		- **Rombo relleno.**
	- **Por Referencia**:
		- Relación también llamada **Agregación**.
		- Tipo de relación **dinámica**.
		- El **tiempo de vida del objeto incluido es independiente del que lo incluye.**
		- **Rombo vacío.**
### <font style="color:#08F">Asociación</font>
![[Pasted image 20250326194150.png]]
- Permite asociar objetos que colaboran entre sí.
- El **tiempo de vida de un objeto no depende del otro.**
### <font style="color:#08F">Dependencia o Instanciación (uso)</font>
- Una instancia es un objeto creado a partir de una clase.
- Se denota con una flecha punteada.
![[Pasted image 20250326194702.png]]
# Generar código a partir de diagramas de clases
- Visual Studio Ultimate
- Umbrello
# Generar diagramas de clases a partir de código
- Visual Studio Code Ultimate.
- Netbeans.
- Eclipse.
	- [Generar diagramas de clases en Eclipse (Java) en 2025 con Eclipse 2024-12: Win y Mac](https://youtu.be/6ha62S8E_5I?si=Qii213BzBaQdekBA)
	- UML Lab Modeling IDE.
![[Pasted image 20250326200212.png]]
![[Pasted image 20250326201002.png]]


