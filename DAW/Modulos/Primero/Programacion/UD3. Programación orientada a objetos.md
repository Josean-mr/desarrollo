# 1. Introducción a la programación orientada a objetos (POO).
La programación Orientada a Objetos en adelante POO es una metodología que basa la estructura de los programas en torno a clases y objetos.
## <font style = "color:salmon">1.1 Clase</font>
- La clase es la unidad de modularidad en el POO.
- La clase permite describir un conjunto de características comunes para los objetos que representa.
- La clase consta de [[07.2_Atributos]] y [[07.3_Métodos]].
### <font style="color:orange">Atributos</font>:
- Son los datos o variables que caracterizan a una clase y cuyos valores en un momento dado indican su estado.
- Sintaxis:
	- `<Modo de Acceso o visibilidad> <Tipo de dato> <Nombre del Atributo>;`
	- <font style="color:green">Ejemplo</font>:
		- public int suma;
#### Modos de acceso para atributos y métodos:

| Modificador<br>de acceso                                         | Misma clase<br>o anidada                | Clase en el<br>mismo<br>paquete         | Clase que<br>hereda en<br>otro paquete<br>(o subclase) | Clase que no<br>hereda en<br>otro paquete |
| ---------------------------------------------------------------- | --------------------------------------- | --------------------------------------- | ------------------------------------------------------ | ----------------------------------------- |
| <font style = "color: green">private</font>                      | <font style = "color:#2980b9">Sí</font> | <font style = "color:#dc7633">No</font> | <font style = "color:#dc7633">No</font>                | <font style = "color:#dc7633">No</font>   |
| <font style = "color: green">default</font> (package<br>private) | <font style = "color:#2980b9">Sí</font> | <font style = "color:#2980b9">Sí</font> | <font style = "color:#dc7633">No</font>                | <font style = "color:#dc7633">No</font>   |
| <font style = "color: green">protected</font>                    | <font style = "color:#2980b9">Sí</font> | <font style = "color:#2980b9">Sí</font> | <font style = "color:#2980b9">Sí</font>                | <font style = "color:#dc7633">No</font>   |
| <font style = "color: green">public</font>                       | <font style = "color:#2980b9">Sí</font> | <font style = "color:#2980b9">Sí</font> | <font style = "color:#2980b9">Sí</font>                | <font style = "color:#2980b9">Sí</font>   |
- **Público**:
	- Son accesibles desde fuera de la clase.
	- Pueden ser llamados por cualquier clase.
	- Símbolo con el que se representa:
		- "+"
- **Privado**:
	- Sólo son accesibles dentro de la implementación de la clase.
	- Símbolo con el que se representa:
		- "-"
- **Protegido**:
	- Accesibles  para su clases y sus clases hijas (subclases).
	- Símbolo con el que se representa.
		- "#"
### <font style="color:orange">Método</font>:
- Son las operaciones (acciones o funciones) que se aplican sobre los objetos y que permiten crearlos, cambiar su estado o consultar el valor de sus atributos.
- Sintaxis:
	- `<Modo de Acceso o visibilidad> <Nombre del método> ([Lista de parámetros]);`
	- <font style="color:green">Ejemplo</font>:
		![[Pasted image 20241222113128.png]]
		- [Link]([▷ Parámetros en JAVA → 【 Cómo usar en JAVA 】](https://oregoom.com/java/parametros/))
		- [07.3_Métodos](obsidian://open?vault=NotasObsidian&file=Programaci%C3%B3n%2FLenguajes%2FJAVA%2F07.3_M%C3%A9todos)
	- <font style="color:green">Ejemplo</font>:
		`public class Rectangulo {`
		    `// Atributos`
		    `private double largo;`
		    `private double ancho;`

		    // Constructor
		    public Rectangulo(double largo, double ancho) {
		        this.largo = largo;
		        this.ancho = ancho;
			}

		    // Método para calcular el área
		    public double calcularArea() {
		        return largo * ancho;
		    }

		    // Método para calcular el perímetro
		    public double calcularPerimetro() {
		        return 2 * (largo + ancho);
		    }

		    // Método para mostrar dimensiones
		    public void mostrarDimensiones() {
		        System.out.println("Largo: " + largo);
		        System.out.println("Ancho: " + ancho);
		    }
		    
		    // Métodos Get y Set para modificar atributos
		    public double getLargo() {
		        return largo;
		    }
		
		    public void setLargo(double largo) {
		        this.largo = largo;
		    }
		
		    public double getAncho() {
		        return ancho;
		    }
		
		    public void setAncho(double ancho) {
		        this.ancho = ancho;
		    }
		`}`
		- [Link Chat GPT](https://chatgpt.com/share/6767ed2e-7e74-8009-94b1-31f3c2d7f7de)
![[Pasted image 20241222125432.png]]
