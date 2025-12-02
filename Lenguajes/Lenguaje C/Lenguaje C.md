## [[Sintaxis C]]

- El tipo de anotación es [[camelCase]].
- Los saltos de línea se realizan con  "\\n".
- Los espacios y los saltos en línea se ignoran hasta el ";".
## [[Librerias C]]

Las librerías se han de agregar antes de la compilación del código.
Algunas de las más comunes son:
- `<stdio.h>`  -> Estándar
- `<stdbool.h>` -> [[Buleanos]] 
- `<math.h>` ->  Constantes matemáticas como potencias
## [[Variables y tipos de datos C]]
### Tipos de variables
#### Variables

| **Variable** | **Tipo**        | **Bytes** | **Imprime** | Notas                            |
| ------------ | --------------- | --------- | ----------- | -------------------------------- |
| `int`        | entero          | 4         | `%i`        |                                  |
| `float`      | real            | 4         | `%f`        |                                  |
| `double`     | mayor que float | --        | `%lf`       | `%lf.9` // define 9 decimales    |
| `char`       | caracter        | 1         | `%c`        |                                  |
| `char`       | cadena          |           | `%s`        | `char cadena[20] = "Mi cadena";` |
| `bool`       | lógico          | 1         |             | necesita librería `<stdbool.h>`  |
#### Constantes

- Las constantes son variables de solo lectura, por lo que no se puede modificar su valor.
- Se suelen definir con mayúsculas.
##### Definir constantes
###### En el código
	const int MI_CONSTANTE = 10;
###### Antes de la compilación del código
// Se define la constante "Renglones" con el valor de 2
	`#define Renglones 2`
- Existen algunas constantes predefinidas:
	- `printf("Valor constante de PI = %.4f", PI);`
- Con constantes matemáticas se ha de añadir la librería `<math.h>`

### Introducir datos
#### Código duro
- Ejemplo:
	- `int miNumero = 10; // Declara la variable miNumero y le asigna el valor de 10.`
#### Dinámicamente
- Cadenas:
	- `scanf("%[^'\n']s", nombre); // Se leen todos los caracteres hasta llegar a "\n"`
	- `fgets(nombre, tamanio_cadena, stdin); // Código seguro`
	- `gets(nombre);`
- Enteros y flotantes:
	- `scanf("%d", &miNumero); // se agrega "&" para apuntar a una dirección de memoria.

## [[Operadores C]]
### Aritméticos

| **Tipo**       | **Operador**                               |                                         |
| -------------- | ------------------------------------------ | --------------------------------------- |
| suma           | `a = 3 + 4;`                               |                                         |
| resta          | `a = 4 - 3;`                               |                                         |
| multiplicación | `a = 3 * 4;`                               |                                         |
| división       | `d = 4 / 2;`                               |                                         |
| módulo         | `f = 6 % 3;`                               |                                         |
| potencia       | `a = pow(4, 2); // se eleva 4 al cuadrado` | se debe utilizar la librería `<math.h>` |
### Incremento y decremento
#### Incremento
- `++variable // se incrementa el valor antes`
- `variable++ // se incrementa el valor después`
#### Decremento
- `--variable // se decrementa el valor antes`
- `variable-- // se decrementa el valor después`
### Asignación
- `miNumero = 10; // tiene el valor de 10`
- `miNumero += 5; // aumenta el valor en 5`
- `miNumero -= 3, // reduce su valor en 3`
- `miNumero *= 2; // multiplica su valor por 2`
- `miNumero /= 7; // divide su valor entre 7`
- `miNumero %=2; // obtiene el módulo de la división entre 2`
### Relacionales
Se pueden utilizar con una sentencia IF para comprobar la relación.
- `c = a == b; // igualdad`
- `c = a != b; // distinto`
- `c = a > b; // mayor que`
- `c = a >= b; // mayor o igual que`
- `c = a < b; // menor que`
- `c = a <= b; // menor o igual que`
### Lógicos
bool // agregar libreria <stdbool.h>
- `variable || variable; // OR`
- `variable && variable; // AND`
- `!variable; // NOT`
Ejemplo de código:
`#include <stdio.h>`
`#include <stdbool.h>`
`int main() {`
	`bool a = true; // Verdadero - 1`
	`bool b = false; // Falso - 0`
	`printf("Valor a: %d", a);`
	`printf("\nValor b: %d", b);`
	
	`// Operador Logico && (and o Y)`
	`// Regresar verdadero si ambos operando son verdaderos`
	`bool c = a && b;`
	`printf("\nResultado operador and '&&': %d", c);`
	
	`// Operador Logico || (or o O)`
	`// Regresa verdadero si cualquiera de los operandos es verdadero`
	`c = a || b; printf("\nResultado operador or '||': %d", c);`
	
	`// Operador Logico ! (Not o No)`
	`// Invierte el valor original, de 1 a 0, o de 0 a 1`
	`c = !a; printf("\nResultado operador not '!' en variable a: %d:", c);`
	`return 0;` 
`}`
## [[Sentencias de decisión]]

### if
#### Sintaxis
- **if** -> Declarar sentencia y comprobar si se cumple la condición
- **else if** -> Comprobar si se cumple una segunda condición. O tercera, cuarta, etc...
- **else** -> Argumentos si no se cumple ninguna condición.
#### Ejemplos según número de condiciones:
#### 1 condición
`if (testCondition) {`
`statements`
`}`
#### 2 condiciones
`if (tesCondition) {`
`statements`
}
`else`  (// resto condiciones) `{`
`statements`
}
#### 3 condiciones o más
`if (testCondition) {`
`statements`
`}`
`else if (testCondition2) {`
`statements`
`}`
`else` (// resto condiciones) `{`
`statements`
`}`

### switch
#### Sintaxis
**switch** -> declarar sentencia.
**case** -> define un caso. Ejemplo: `case 1:`
**break** -> si un caso se cumple, establece que el ciclo no siga validando otros casos.
**default** -> define un argumento por defecto en caso de que no se cumpla ningún caso.
##### Ejemplo
`switch (numeroDia) {`
		`case 1:`
			`printf("Lunes");`
			`break; // se utiliza para no seguir valorando el resto de casos`
		`case 2:`
			`printf("Martes");`
			`break;`
		`case 3:`
			`printf("Miercoles");`
			`break;`
		`case 4:`
			`printf("Jueves");`
			`break;`
		`case 5:`
			`printf("Viernes");`
			`break;`
		`case 6:`
			`printf("Sabado");`
			`break;`
		`case 7:`
			`printf("Domingo");`
			`break;`
		`default:`
			`printf("Valor dia erroneo: %d", numeroDia);`
	`};`
## [[Ciclos C]]

### while

#### Sintaxis
**while** -> declara el ciclo.
#### Ejemplo
#include <stdio.h>
#include <stdbool.h>

`int main() {`
	
	// Ciclo while
	// Definir las variables
	int contador = 0, repeticiones = 5;
	// ciclo while
	while (contador < repeticiones) {
		printf("\nBuenos dias... %d\n", contador);
		
		// Incrementar el valor de contador en cada iteracion
		contador++;
		
		// Declarar variable buleana para indicar el numero de iteracion
		bool condicion = contador < repeticiones;
		printf("%d < %d -> %d \n", contador, repeticiones, condicion);
	}
	
	printf("\nYa hemos salido del ciclo while.");
	return 0;
}
### do while
#### Sintaxis
**do** -> declara el ciclo.
**while** -> establece la condicion que, hasta que no sea falsa, no se sale del ciclo.
#### Ejemplo
`#include <stdio.h>`

`int main() {`
	`// Validar que el usuario introduzca un numero positivo`
	`int numeroPositivo;`
	`// do-while -> Repetir en Pseint`
	`do{`
		`printf("\nIntroduce un numero positivo: \n");`
		`scanf("%d", &numeroPositivo);`
	`} while(numeroPositivo <= 0); // termina cuando la condicion sea falsa`
	`printf("Se ha salido de ciclo do while (repetir).\n");`
	`return 0;`
}
### for
#### Sintaxis
**for** -> Declara el ciclo for.
#### Ejemplo
`#include <stdio.h>`

`int main() {`
	`// Ciclo for`
	`for (int contador = 1; contador <= 5; contador++) {`
		`printf("\nBuenos dias");`
		`printf("\nVariable contador: %d\n", contador);`
	`}`
	`return 0;`
`}
## [[Arreglos C]]
### Declaración de arreglos
#### Código duro
`int numerosArreglo[5];`
int *arg
#### Código dinámico
`scanf("%d", &arreglo[5]);` -> '&' porque solo se utiliza un elemento individual del arreglo.
##### Código dinámico cadenas
- `scanf("%[^'\n']s", nombre); // Se leen todos los caracteres hasta llegar a "\n"`
- `fgets(nombre, tamanio_cadena, stdin); // Código seguro`
- `gets(nombre);`
### Modificar valor arreglo
// se modifica el valor a 13.
`numeroArreglo[0] = 13;` 
### Leer valor arreglo
`printf("%d", numeroArreglo[0]);`
### Iteración arreglo
#### Leer

	for (int i = 0; i < tamanioArreglo; i++) {
		printf("\n[%d] Valor %d del arreglo: ", i, i + 1);
		scanf("%d", &arreglo[i]); // Se pone '&' porque solo se utiliza un elemento individual del arreglo
	}
#### Imprimir
`printf("\nLos valores del arreglo introducidos son: ");`
	`for (int i = 0; i < tamanioArreglo; i++) {`
		`printf("\nValor[%d] = %d", i, arreglo[i]); // Para imprimir el texto no se escribe '&'`
	`}`
### Calcular el tamaño de un arreglo
#### sizeof
1. Declarar variable para el tamaño del arreglo:
	1. Para calcular el tamaño del arreglo entero:
		1. `int tamanioArreglo = sizeof(arreglos);`
	2. Para calcular el tamaño de una celda del arreglo:
		1. `int tamanioUnElemento = sizeof(arreglos[0]);`
2. Obtener la longitud del arreglo con el tamaño del arreglo entero y el tamaño de un elemento del arreglo:
	1. `int longitudArreglo = tamanioArreglo / tamanioUnElemento;`
## [[Matrices C]]
### Declaración matriz
#### Código duro
// declaración de matriz con 2 renglones y 2 columnas
`int matriz[2][2];`
#### Código dinámico
// declarar variables que contendrán el numero de renglones y columnas
`int RENGLONES;`
`int COLUMNAS;`
// Leer el numero de renglones y columnas para asignarles valor
`scanf("%d", &RENGLONES);`
`scanf("%d", &COLUMNAS);`
// Declarar la matriz que contendrá el valor de renglones y columnas introducidas dinámicamente
`int matriz[RENGLONES][COLUMNAS];`
### Modificar valor matriz
`matriz[0][0] = 100;`
### Leer valor matriz
`printf("%d", matriz[0][0]);`
### Sintaxis simplificada
#### Método 1
 // Los valores son asignados a las renglones de izquierda a derecha y de arriba a abajo.
`int matriz[RENGLONES][COLUMNAS] =`
`{100, 200, 300, 400, 500, 600};`
#### Método 2
 // Cada renglón está agrupada entre llaves y se separan por comas entre renglones. De modo que es más visual si se utiliza el salto de línea detrás de cada renglón.
`int matriz[RENGLONES][COLUMNAS] =`
	`{`
			`{100, 200, 300},`
			`{400, 500, 600}`
	`};`
## Iterar la matriz
// Iterar la matriz
// Declarar variable renglón para que haga de pivote
`for(int renglon = 0; renglon < RENGLONES; renglon++) {`
	`printf("\n\nRenglon pivote: %d", renglon);`
	// Declarar la variable columna para que itere hasta llegar al valor del número de columnas
	`for(int columna = 0; columna < COLUMNAS; columna++) {`
		`printf("\nMatriz[%d][%d] = %d", renglon, columna, matriz[renglon][columna]);`
	`}`
`}`
## Introducir valores en matriz
`#include <stdio.h>`

`int main() {`
	`// Declarar las variables para el numero de renglones y columnas`
	`int renglones;`
	`int columnas;`
	`printf("Introduce el numero de renglones de la matriz: \n");`
	`scanf("%d", &renglones);`
	`printf("Introduce el numero de columnas de la matriz: \n");`
	`scanf("%d", &columnas);`
	
	// Declarar matriz
	int matriz[renglones][columnas];
	
	// Iterar la matriz para introducir los datos
	// Declarar variable renglon para que haga de pivote
	for(int renglon = 0; renglon < renglones; renglon++) {
		printf("\n\nRenglon pivote: %d", renglon);
		// Declarar la variable columna para que itere hasta llegar al valor del numero de columnas
		for(int columna = 0; columna < columnas; columna++) {
			printf("\nIntroducir valor matriz[%d][%d]: ", renglon, columna);
			scanf("%d", &matriz[renglon][columna]); // '&' porque lo posicionamos en la direccion de memoria de la celda de la matriz
		}
	}
	
	printf("Valores introducidos en la matriz");
	// Imprimir la matriz
	// Declarar variable renglon para que haga de pivote
	for (int renglon = 0; renglon < renglones; renglon++) {
		printf("\n\nRenglon pivote: %d", renglon);
		// Declarar la variable columna para que itere hasta llegar al valor del numero de columnas
		for (int columna = 0; columna < columnas; columna++) {
			printf("\nMatriz[%d][%d] = %d", renglon, columna, matriz[renglon][columna]);
		}
	}
	return 0;
}
## [[Funciones en C]]
### Procedimientos
- Son funciones que realizan una tarea específica y no devuelven un valor.
- Se declaran con `void`.
#### Ejemplo
`#include <stdio.h>`

`// Definir la funcion (procedimiento) saludar`
`// Se utiliza 'void' porque no regresa ninguna informacion a la funcion principal`
`void saludar(char mensaje[]){`
	`printf("Mensaje: %s\n", mensaje);`
`}`

`int main() {`
	`// Ejercicio para definir una funcion`
	`char argMensaje[50];`
	`printf("Proporciona el mensaje a mostrar: \n");`
	`// solicitar ingresar el mensaje`
	`// sin '&' porque se pasa el valor por referencia`
	`scanf("%[^\n]s", argMensaje);`
	`// llamar la funcion 'saludar'`
	`saludar(argMensaje);`
	`saludar(argMensaje);`
	`saludar(argMensaje);`
	
	`return 0;`
`}
### Funciones
- Es un bloque de código que realiza una tarea específica y puede devolver un valor.
#### Ejemplo
`#include <stdio.h>`

`// definir la funcion sumar`
`// se declaran las variables y el tipo de variable`
`int  sumar(int a, int b){`
	`// se declara una variable para que contenga el resultado de la suma de los argumentos`
	`int resultadoSuma = a + b;`
	`// regresar el resultado de la suma`
	`return resultadoSuma;`
	`// a continuacion de 'return' ya no se puede agregar mas codigo`
`}`

`int main() {`
	`// ejercicio funcion sumar`
	`// declarar las variables y el tipo de variable`
	`int argA, argB, resultado;`
	`// solicitar los valores`
	`printf("Proporciona el valor del primer argumento: \n");`
	`scanf("%d", &argA);`
	`printf("Proporciona el valor del segundo argumento: \n");`
	`scanf("%d", &argB);`
	
	`// llamar la funcion sumar`
	`resultado = sumar(argA, argB);`
	`printf("el resultado de sumar %d + %d es: %d\n", argA, argB, resultado);`
	
	`return 0;`
`}`
