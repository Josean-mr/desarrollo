### Aritmeticos

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