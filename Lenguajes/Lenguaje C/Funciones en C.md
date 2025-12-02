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
## <font style="color:orange">Formas de pasar la información a las funciones</font>
Hay 2 formas de pasar la información (argumentos) a la función:
- **Por Valor.**
- **Por Referencia.**
### <font style="color:yellow">Por Valor</font>
- **Se pasa una copia del valor**.
- **La función invocada no modifica el valor de la variable en la función principal.**
- <font style="color:LightSalmon">Ejemplo:</font>
`#include <stdio.h>`

`// Funcion cambiarValor (parametro por valor)`
`void cambiarValor(int parametro) {`
	`printf("\n2. Se ha invocado la funcion y se ha copiado el valor a la variable parametro: %d", parametro);`
	`parametro = 20;`
	`printf("\n3. Se ha modificado el valor de la variable parametro con 20: %d", parametro);`
`}`

`int main() {`
	`// Ejemplo de paso por valor`
	`int argumento = 10;`
	`printf("1. argumento tiene el valor de 10: %d", argumento);`
	`cambiarValor(argumento);`
	`printf("\n4. Se a vuelto a algoritmo princial, la funcion no ha modificado el valor de la variable en el algoritmo principal: %d", argumento);`
	
	`return 0;`
- <font style="color:lightsalmon">Resultado:</font>
1. Argumento tiene el valor de 10: 10

2. Se ha invocado la funcion
y se ha copiado el valor a la variable parametro: 10

3. Se ha modificado el valor
de la variable parametro con 20: 20

4. Se ha vuelto a la funcion principal, la funcion
no ha modificado el valor de la variable en la funcion principal: 10

<< Program finished: exit code: 0 >>
<< Press enter to close this window >>
### <font style="color:yellow">Por Referencia</font>
- **Se pasa la dirección de memoria** en lugar de una copia del valor de la variable.
- **Cualquier cambio que se realice en la función se verá reflejado en la variable de la función principal** ya que las variables de la función y la función principal apuntan a la misma dirección de memoria.
- Aunque se utilice la funcion void, se modifica el valor de la variable de la función principal.
- <font style="color:LightSalmon">Ejemplo:</font>
`#include <stdio.h>`

`void cambiarValor(int *parametro) {`
	`printf("\n2. Se ha invocado la funcion, valor variable parametro: %d. \nSe ha pasado la direccion de memoria que sigue siendo %p\n", *parametro, parametro);`
	`*parametro = 20;`
	`printf("\n3. Se ha modificado el valor de la variable a %d. \nLa direccion de memoria es: %p\n", *parametro, parametro);`
`}`

`int main() {`
	`// Ejercicio del Paso por Referencia`
	`int argumento = 10;`
	`printf("1. Valor del argumento en funcion principal: %d. \nDireccion de memoria: %p\n", argumento, &argumento);`
	`cambiarValor(&argumento);`
	`printf("\n4. Valor del argumento en funcion principal: %d. \nDireccion de memoria: %p\n", argumento, &argumento);`
	`printf("\nEn resumen. La direccion de memoria ha sido todo el tiempo la misma \ny se ha modificado el valor que contiene la direccion de memoria.");`
	
	`return 0;`
`}`
- <font style="color:lightsalmon">Resultado:</font>
1. Valor del argumento en funcion principal: 10. 
Direccion de memoria: 0x7ffe9b48bd54

2. Se ha invocado la funcion, valor variable parametro: 10. 
Se ha pasado la direccion de memoria que sigue siendo 0x7ffe9b48bd54

3. Se ha modificado el valor de la variable a 20. 
La direccion de memoria es: 0x7ffe9b48bd54

4. Valor del argumento en funcion principal: 20. 
Direccion de memoria: 0x7ffe9b48bd54

En resumen. La direccion de memoria ha sido todo el tiempo la misma 
y se ha modificado el valor que contiene la direccion de memoria.

<< Program finished: exit code: 0 >>
<< Press enter to close this window >>
#### [[Arreglos C]]
- Los arreglos siempre se pasan por referencia.
- Se puede declarar los arreglos de varias maneras:
	- Indicando que es un arreglo:
		- `int arg[] = {1, 2, 3};`
	- Utilizando el apuntador:
		- `int *arg = {1, 2, 3};`
- <font style="color:LightSalmon">Ejemplo:</font>
`#include <stdio.h>`

`/* Con asterisco, se indica que es un apuntador a un arreglo.`
`Tambien se puede declarar la variable como arreglo[] */`
`void cambiarValor(int *parametro) {`
	`printf("\n2. Se ha invocado la funcion. ");`
	`parametro[0] = 4;`
	`parametro[1] = 5;`
	`parametro[2] = 6;`
	`printf("\n3. Se ha modificado el valor del arreglo.");`
`}`

`int main() {`
	`// Ejercicio del Paso por Referencia`
	`int arg[] = {1, 2, 3};`
	`// int *arg = {1, 2, 3}; // Tambien se pueden definir los arreglos con el apuntador`
	`printf("1. Valor del arg en funcion principal: \n[0] = %d \n[1] = %d \n[2] = %d\n", arg[0], arg[1], arg[2]);`
	`/* Los arreglos siempre se pasan por referencia.`
	`No se necesita especificar su dirección de memoría con "&" porque`
	`el nombre del array se convierte en el puntero al primer elermento del array */`
	`cambiarValor(arg);`
	`printf("\n4. De vuelta a la funcion principal: \n[0] = %d \n[1] = %d \n[2] = %d\n", arg[0], arg[1], arg[2]);`
	`printf("\nEn resumen. La direccion de memoria ha sido todo el tiempo la misma \ny se ha modificado el valor que contiene la direccion de memoria del arreglo.");`
	
	`return 0;`
`}`
- <font style="color:LightSalmon">Resultado:</font>
1. Valor del arg en funcion principal: 
[0] = 1 
[1] = 2 
[2] = 3

2. Se ha invocado la funcion. 
3. Se ha modificado el valor del arreglo.
4. De vuelta a la funcion principal: 
[0] = 4 
[1] = 5 
[2] = 6

En resumen. La direccion de memoria ha sido todo el tiempo la misma 
y se ha modificado el valor que contiene la direccion de memoria del arreglo.

##### Cadenas que no modifican su valor de la función principal
- Las cadenas se pasan por referencia.
- La variable puede cambiar de valor durante una función, pero cuando vuelve a la función principal recupera el valor de la función principal.
- <font style="color:LightSalmon">Ejemplo:</font>
`#include <stdio.h>`

`/* Con asterisco, se indica que es un apuntador a un arreglo.`
`Tambien se puede declarar la variable como arreglo[] */`
`void cambiarValor(char *parametro) {`
	`parametro = "Adios";`
	`printf("2. Durante la llamada a la funcion: %s\n", parametro);`
	`int argTamanioFuncion;`
	`argTamanioFuncion = sizeof(parametro);`
	`printf("2.1 Tamanio del arreglo durante la funcion = %d bytes \n", argTamanioFuncion);`
`}`

`int main() {`
	`// Ejercicio del Paso por Referencia`
	`char arg[] = "Hola";`
	`// char *arg = "Hola";`
	`printf("1. Antes de llamar a la funcion: %s\n", arg);`
	
	// Invocar la funcion
	cambiarValor(arg);
	printf("3. Despues de llamar a la funcion: %s\n", arg);
	
	int argTamanio;
	argTamanio = sizeof(arg);
	printf("3.1 Tamanio del arreglo despues de llamar a la funcion = %d bytes \n", argTamanio);
	
	return 0;
}

- <font style="color:LightSalmon">Resultado:</font>
1. Antes de llamar a la funcion: Hola
2. Durante la llamada a la funcion: Adios
2.1 Tamanio del arreglo durante la funcion = 4 bytes
3. Despues de llamar a la funcion: Hola
3.1 Tamanio del arreglo despues de llamar a la funcion = 5 bytes


<< Program finished: exit code: 0 >>
<< Press enter to close this window >>
#### [[Modificación de cadena en paso por referencia C]]
- Los tipos de datos han de coincidir tanto en la función principal como en la función.
	- Se ha de utilizar el apuntador de memoria "*"(asterisco).
	- Cuando se vuelve a la función principal se ha de asignar a la variable de la función principal el valor de la función.
		- `arg = cambiarValor(arg);`
- <font style="color:LightSalmon">Ejemplo:</font>
`#include <stdio.h>`

`/* Con asterisco, se indica que es un apuntador a un arreglo.`
`Tambien se puede declarar la variable como arreglo[] */`
`char *cambiarValor(char *parametro) {`
	`parametro = "Adios";`
	`printf("2. Durante la llamada a la funcion: %s\n", parametro);`
	`// Retornar el valor`
	`return parametro;`
`}`

`int main() {`
	`// Ejercicio del Paso por Referencia`
	`// char arg[] = "Hola";`
	`char *arg = "Hola";`
	`printf("1. Antes de llamar a la funcion: %s\n", arg);`
	
	// Invocar la funcion
	arg = cambiarValor(arg);
	printf("3. Despues de llamar a la funcion: %s\n", arg);	
	
	int argTamanio;
	argTamanio = sizeof(arg);
	printf("3.1 Tamanio del arreglo despues de llamar a la funcion = %d bytes \n", argTamanio);
	
	return 0;
`}`
- <font style="color:LightSalmon">Resultado:</font>
1. Antes de llamar a la funcion: Hola
2. Durante la llamada a la funcion: Adios
3. Despues de llamar a la funcion: Adios
3.1 Tamanio del arreglo despues de llamar a la funcion = 4 bytes
