# 1. Visión histórica
La **Informática** es la ciencia del tratamiento automático y racional de la información.
## <font style = "color:salmon">Tipos o niveles de lenguajes</font>
![[Pasted image 20240919195827.png]]
### <font style = "color:orange">Lenguaje máquina o binario</font>
- El **primer lenguaje de programación**.
- Es de bajo nivel.
- Depende del hardware.
- **Muy difíciles de utilizar**, por lo que se creo el lenguaje ensamblador.
- Ejemplo de instrucción:
	- 01001001 10010010 11000011 00001111

### <font style = "color:orange">Lenguaje ensamblador</font>
- Más sencillos que el lenguaje máquina.
- Es de bajo nivel.
- Depende del hardware.
- Están definidos por un código nemotécnico que establece una cierta equivalencia entre las instrucciones del código máquina y las instrucciones del lenguaje ensamblador.
- Ejemplo de instrucción:
	- MOV AX, 5 ; Mueve el valor 5 al registro AX
	- ADD AX, 3 ; Suma el valor 3 al registro AX
### <font style = "color:orange">Lenguaje de alto nivel</font>
- Lenguaje más cercano al lenguaje natural.
- El lenguaje es independiente de la máquina.
- Son los que se utilizan a día de hoy.
- Son independientes de la arquitectura del ordenador.
- Tienen que ser compilados a lenguaje máquina.
- Ejemplo de instrucción:
		- int x = 5;
# 2. La programación de ordenadores
## <font style = "color:salmon">Metodología de la programación</font>
### <font style = "color:orange">Metodología estructurada y modular</font>
También conocida como metodología tradicional.
### <font style = "color:orange">Metodología orientada a objetos</font>
Enfoque más avanzado y que se basa en el concepto de **"objetos"** que interactúan entre sí.
#### <font style = "color:green">Ventajas</font>
##### <font style = "color:khaki">La encapsulación</font>
Agrupación de datos y métodos en una sola entidad llamada clase y ocultación de la misma a otras partes del código.
##### <font style = "color:khaki">El polimorfismo</font>
Capacidad de un objeto para comportarse de diferentes formas según el contexto.
##### <font style = "color:khaki">Modularidad</font>
Favorece el desarrollo y mantenimiento de forma independiente y la reutilización del código.
##### <font style = "color:khaki">La herencia</font>
Creación de nuevas clases basadas en otras.
### Esencia de la metodología de programación
Se basa en el empleo de técnicas de programación estructurada, que consisten en:
	<font style = "color:orange">1. </font> Desarrollar un programa en módulos con diseño descendente (descomponer el problema en partes más pequeñas).
	<font style = "color:orange">2. </font>Emplear únicamente tres clases de estructuras básicas de control (secuencial, alternativa, y repetitiva) en el desarrollo de cada módulo.
# 3. Concepto de algoritmo
Un algoritmo es un **conjunto de acciones u operaciones a realizar por el ordenador, así como el orden en que se deben ejecutar.**
## <font style = "color:salmon">Resolución de problemas</font>
La resolución de todo problema exige el diseño de un algoritmo, y los pasos para dicha resolución son:
![[Pasted image 20240919204528.png]]
### <font style = "color:orange">1. Análisis del problema</font>
Definir y comprender el problema a resolver.
### <font style = "color:orange">2. Diseño del algoritmo</font>
Describir la secuencia de pasos que conducen a la solución del problema planteado.
### <font style = "color:orange">3. Programa de ordenador</font>
Traducir el algoritmo a un lenguaje de programación para que el ordenador pueda ejecutarlo.
### <font style = "color:orange">4. Ejecución y valoración del programa</font>
Ejecutar el programa y comprobar que los resultados obtenidos son los esperados.
## <font style = "color:salmon">Características del algoritmo</font>
Las características fundamentales que debe cumplir todo algoritmo son:
![[Pasted image 20240919205053.png]]
# 4. Lenguajes de programación
## <font style = "color:salmon">Lenguaje compilado o interpretado</font>
### <font style = "color:orange">Lenguaje compilado</font>
- Existe un traductor que recoge el programa realizado por el programador y lo compila para un determinado sistema operativo.
- Ejemplos:
	- C, C++, C#, SWIFT...
![[Pasted image 20240920170351.png]]
### <font style = "color:orange">Lenguaje interpretado</font>
- Son lenguajes que necesitan un intérprete para ser ejecutados.
- Ejemplos:
	- PHP, JavaScript, Ruby...
![[Pasted image 20240920170406.png]]
### JAVA
- Se encuentra entre lenguaje compilado e interpretado.
- El compilador traduce el código de alto nivel a un código intermedio llamado bytecode.
	- El código bytecode se puede distribuir a cualquier plataforma.
		- El ordenador destino requiere el ejecutor Java Virtual Machine (JVM) para poder ejecutar el código. 
![[Pasted image 20240920170452.png]]
# 5. Datos y tipos de datos
Link al curso de Java -> [[02. Variables]]
![[Pasted image 20240920174120.png]]
# 6. Constantes y variables
- Cuando se declara una constante o una variable se está reservando un espacio en memoria en el que se almacenará el valor.
- Lo normal es declarar todas las variables al inicio del algoritmo o programa, pero otras veces se declaran según se van necesitando.
- Se pueden declarar agrupar variables del mismo tipo en el momento de la declaración.
## <font style = "color:salmon">Constantes</font>
Valores que no deben cambiar durante la ejecución del programa.
- Ejemplo de sintaxis:
	- `CONSTANTE nombre_constante = valor`
## <font style = "color:salmon">Variables</font>
Valores que cambian durante la ejecución del programa.
- Ejemplo de sintaxis:
	- `_tipo_de___dato_` `nombre o identificador;`
# 7. Expresiones
Combinación de constantes, variables, símbolos de operaciones, paréntesis y nombre de funciones especiales, de cuya evaluación se obtiene un único resultado.
![[Pasted image 20240920181456.png]]
## <font style = "color:salmon">Expresión aritmética</font>
- Compuesta por operaciones matemáticas:
	- Suma: +
	- Resta: -
	- Multiplicación: *
	- División: /
	- Resto: %, Mod
## <font style = "color:salmon">Expresión lógica</font>
- Devuelve un valor lógico o booleano.
- Se pueden utilizar operadores relacionales u operadores lógicos.
## <font style = "color:salmon">Orden de prioridad</font>
1. ( )
2. ^ , no
3. * , / , div , mod, y
4. + , - , o
5. operaciones relacionales (>, <, >=, <=, =, !=)
Si todos los operadores tienen el mismo grado de prioridad se evalúa de izquierda a derecha.
# 8. Operaciones de asignación
Link al curso de Java -> [[04. Operadores]]
- Es una de las formas de proporcionar valor a las variables.
- Es una operación destructiva.
# 9. Representación de algoritmos. Software de utilidad.
## <font style = "color:salmon">Varias formas de representar instrucciones</font>
- Diagramas de flujo.
- Diagramas de N-S (Nassi-Shneiderman): elementos y ejemplos.
- Pseudocódigo.
### <font style = "color:orange">1. Diagramas de flujo</font>
- Utiliza símbolos gráficos denominados cajas.
- Las cajas están conectadas mediante líneas de flujo.
[Enlace a editor de diagrama de flujo DIA](https://sourceforge.net/projects/dia-installer/)
![[Pasted image 20240920192153.png]]
![[a6af1547-5dce-420c-ba2e-c1fac83dd205.png]]
### <font style = "color:orange">2. Diagramas de N-S (Nassi-Shneiderman)</font>

- Como el diagrama de flujo, pero se eliminan las líneas de flujo.
- Las cajas están continuas unas a otras.
![[Pasted image 20240920192612.png]]![[Pasted image 20240920192655.png]]
### <font style = "color:orange">3. Pseudocódigo</font>
- El tipo de representación más utilizado.
#### <font style = "color:green">PSeInt</font>
[Enlace a PSeInt](https://pseint.sourceforge.net/)
[Enlace a curso YouTube](https://youtu.be/eWdIetuIPNM?si=Nq3HgEC-gpRoTwbk)
##### Identificadores
- Definir nombre al algoritmo:
	- UpperCamelCase
	- lowerCamelCase
- Definir tipo de variable (Ejemplos):
	- **Definir** acierto como **Lógico**.
	- **Definir** suma como **Entero**.
	- **Definir** nombre como **Cadena**.
	- **Definir** total como **Real**.
# 10. Estructuras de control
[[06.1. Estructuras de control (Condicionales)]]
![[Pasted image 20240920195351.png]]
## <font style = "color:salmon">Dos tipos principales de estructuras de control:</font>
- Estructuras selectivas.
- Estructuras repetitivas.
### <font style = "color:orange">Estructuras selectivas (if, swtich)</font>
- Permiten ejecutar una serie de instrucciones u otras dependiendo del valor:
	- De una expresión **booleana**.
	- De una variable:
		- **Numérica**.
		- De **carácter**.
		- De **texto**.
#### <font style = "color:green">Sintaxis en PSeInt</font>
##### <font style = "color:violet">Si (if)</font>
- **Simple:**
`Si condicion Entonces`
	`instrucciones;`
`FinSi`
![[Pasted image 20240921083828.png]]
- **Doble:**
`Si condición Entonces`
	`Instrucciones1;`
`SiNo`
	`Instrucciones2;`
`FinSi`
![[Pasted image 20240921084222.png]]
- **Múltiple:**
`Si condicion1 Entonces`
	`Instruccciones1;`
`SiNo`
	`Si condicion2 Entonces`
		`Instrucciones2;`
	`SiNo`
		`Si condicion3 Entonces`
			`Instrucciones3;`
		`SiNo`
			`Instrucciones4;`
	`FinSi`
`FinSi`
![[Pasted image 20240921085057.png]]
##### <font style = "color:violet">Según (switch)</font>
- Ejemplo:
	`Segun variable_numerica Hacer`
		`1:`
			`Imprimir "Es el número 1"`
		`2:`
			`Imprimir "Es el número 2"`
		`3:`
			`Imprimir "Es el número 3"`
		`4:`
			`Imprimir "Es el número 4"`
		`5:`
			`Imprimir "Es el número 5"`
		`De Otro Modo:`
			`Imprimir "Número no reconocido"`
	`FinSegun`
	![[Pasted image 20240921090107.png]]
### <font style = "color:orange">Estructuras repetitivas (for, while, do-while)</font>
- Permiten ejecutar una serie de instrucciones un número de veces indeterminado que va a depender de:
	- Una expresión booleana.
	- Un número determinado de veces.
#### <font style = "color:green">Sintaxis en PSeInt</font>
##### <font style = "color:violet">Mientras (while)</font>
- Repite una serie de instrucciones mientras se cumple una determinada condición. Es decir, mientras la condición es verdadera.
`Mientras condición Hacer`
	`Instrucciones;`
`FinMientras`
![[Pasted image 20240921092007.png]]
##### <font style = "color:violet">Para (for)</font>
- Ejemplo:
	`Para i = 0 Hasta 10 Con Paso 1 Hacer`
		`Imprimir i`
	`FinPara`
![[Pasted image 20240921101611.png]]
##### <font style = "color:violet">Repetir (do-while)</font>
Se utiliza cuando se quiere repetir una serie de instrucciones hasta que se cumpla una determinada condición. Cuando la condición sea verdadera, el ciclo se termina.
`Repetir`
	`instrucciones;`
`Hasta Que condición`
![[Pasted image 20240921111712.png]]
