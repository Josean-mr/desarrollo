## <font style="color:orange">Tipos de variables</font>
### <font style="color:yellow">Variables</font>

| **Variable** | **Tipo**        | **Bytes** | **Imprime** | Notas                                                                                                    |
| ------------ | --------------- | --------- | ----------- | -------------------------------------------------------------------------------------------------------- |
| `int`        | entero          | 4         | `%i`        |                                                                                                          |
| `float`      | real            | 8         | `%f`        |                                                                                                          |
| `double`     | mayor que float | 8         | `%lf`       | `%lf.9` // define 9 decimales                                                                            |
| `char`       | caracter        | 1         | `%c`        |                                                                                                          |
| `char`       | cadena          |           | `%s`        | `char cadena[20] = "Mi cadena";`                                                                         |
| `bool`       | lógico          | 1         |             | necesita librería `<stdbool.h>`                                                                          |
| `*`          | apuntador       |           | `%d`        | Se le asigna el valor de una variable.<br>Desde el apuntador se puede modificar el valor de la variable. |
#### <font style="color:green">int</font>
##### Declarar y definir valores
- **Código duro:**
	- Solo declarar variable:
		- `int numeroEntero;`
	- Declarar variable y asignar un valor:
		- `int numeroEntero = 10;`
- **Código dinámico:**
	- Primero se debe declarar la variable: `int numeroEntero;`
	- Se utiliza el operador de dirección "&" para pasar la dirección de la variable "numeroEntero" a "scanf".
		- `scanf("%d", &numeroEntero);`
##### Imprimir valores
- `printf("%d", numeroEntero);`
#### <font style="color:green">float</font>
##### Declarar
- **Código duro:**
	- Solo declarar variable:
		- `float numeroReal;`
	- Declarar variable y asignar un valor:
		- `float numeroReal = 10;`
- **Código dinámico:**
	- Primero se debe declarar la variable: `int numeroReal;`
	- Se utiliza el operador de dirección "&" para pasar la dirección de la variable "numeroReal" a "scanf".
		- `scanf("%f", &numeroReal);`
##### Imprimir valores
- Imprimir los decimales por defecto:
	- `printf("%f", numeroReal);`
- Determinar el número de decimales a imprimir (2 en el ejemplo):
	- `printf("%.2f", numeroReal);`
#### <font style="color:green">double</font>
##### Declarar
- **Código duro:**
	- Solo declarar variable:
		- `double numeroReal;`
	- Declarar variable y asignar un valor:
		- `double numeroReal = 10;`
- **Código dinámico:**
	- Primero se debe declarar la variable: `double numeroReal;`
	- Se utiliza el operador de dirección "&" para pasar la dirección de la variable "numeroReal" a "scanf".
		- `scanf("%lf", &numeroReal);`
##### Imprimir valores
- Imprimir los decimales por defecto:
	- `printf("%lf", numeroDouble);`
- Determinar el número de decimales a imprimir (2 en el ejemplo):
	- `printf("%.2lf", numeroDouble);`
#### <font style="color:green">char (carácter)</font>
##### Declarar
- **Código duro:**
	- Solo declarar variable:
		- `char vocalA;`
	- Declarar variable y asignar un valor:
		- `char vocalA = 'A';`
- **Código dinámico:**
	- Primero se debe declarar la variable: `char vocalA;`
	- Se utiliza el operador de dirección "&" para pasar la dirección de la variable "vocalA" a "scanf".
		- `scanf("%c", &vocalA);`
##### Imprimir valores
- Imprimir los decimales por defecto:
	- `printf("%c", vocalA);`
#### <font style="color:green">char (cadena)</font>
##### Declarar
- **Código duro:**
	- Declarar variable y asignar un valor:
		- `char cadenaTexto[15] = "Hola Mundo";`
- **Código dinámico:**
	- Primero se debe declarar la variable: `char cadenaTexto[15];`
	- No se utiliza el operador de dirección "&" porque el nombre del array ya actúa como puntero.
	- Una vez declarada la variable `cadenaTexto[15]`. Existen varios modos de insertar información dinámicamente en una cadena.
		- `fgets(cadenaTexto, sizeof(cadenaTexto), stdin);`// método que evita saturar el buffer.
		- `scanf("%[^'\n']s", cadenaTexto);`
		- `gets(nombre);`
##### Imprimir valores
- Imprimir la cadena entera:
	- `printf("%s", cadenaTexto);`
- Imprimir un carácter de la cadena:
	- `printf("%c", cadenaTexto[1]);`
#### <font style="color:green">bool</font>
Requiere la librería `<stdbool.h>` que se agrega antes de la compilación del código.
##### Declarar
- **Código duro:**
	- Solo declarar variable:
		- `bool verdaderoFalso;`
	- Declarar variable y asignar un valor, 1 para verdadero y 0 para falso:
		- `bool verdaderoFalso = 1;`
- **Código dinámico:**
	- Se declara la variable: `bool verdaderoFalso;` y una variable temporal de tipo entero, ya que deberá almacenar el valor de 1 o 0: `int verdaderoFalsoTemporal;`
	- Con scanf se solicita asignar a la variable temporal el valor de 0 o 1:
	  `scanf("%d", &verdaderoFalsoTemporal);`
	- Se asigna el valor de la variable temporal a la variable buleana:
	  `verdaderoFalso = verdaderoFalsoTemporal;`
##### Imprimir valores
`printf("%d",  verdaderoFalso);`
#### <font style="color:green">* (apuntador)</font>
##### Declarar
- Con "`*`" se declara que la variable almacena la dirección de memoria.
	- Ejemplo de declarar variable de tipo entero que es un apuntador a la dirección de memoria de variable "miNumero".
		- `int *apuntador = &miNumero;`
- Desde el apuntador se puede modificar el valor de la variable.
	- Ejemplo de modificar el valor de variable "miNumero" a 10:
		- `*apuntador = 10;`
##### Imprimir
- Para **imprimir la dirección de memoria** de un apuntador se utiliza el especificador de formato "`%p`". Pero no es necesario utilizar el símbolo "`&`", ya que se ha declarado la variable como apuntador con "`*`".
	- `printf("%p", apuntador);`
- Para **imprimir el valor de la variable** se ha de utilizar el operador "`*`" para desreferenciar el puntero.
	- `printf("%d", *apuntador);`
### <font style="color:yellow">Constantes</font>

- Las constantes son variables de solo lectura, por lo que no se puede modificar su valor.
- Se suelen definir con mayúsculas.
#### Definir constantes
##### En el código
	const int MI_CONSTANTE = 10;
##### Antes de la compilación del código
	#define Renglones 2 // Se define la constante "Renglones" con el valor de 2
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