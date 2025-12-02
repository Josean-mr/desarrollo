# ¿Qué es un array?
- Una secuencia de elementos, en el que cada <font style="color:salmon;font-weight:bold">elemento</font> se asocia con al menos un **índice** (entero no negativo).
- Cada elemento ocupa el <font style="color:salmon;font-weight:bold">mismo numero de bytes</font>.
- Los elementos son del <font style="color:salmon;font-weight:bold">mismo tipo</font>.
- El número de índices es la <font style="color:salmon;font-weight:bold">dimensión</font> del array.
# Declaración de un array de una dimensión
## Utilizar un inicializador.
<font style="color:orange;font-weight: bold">Sintaxis:</font>
```java
type variable_name[] = {valores_variable};
```
<font style="color:green;font-weight: bold">Ejemplo:</font>
```java
String capitales[] = {"Madrid", "Lisboa", "Tallin"};
```
## Utilizar palabra reservada new sin inicializador.
Cuenta con 2 posibles formas:
<font style="color:orange;font-weight: bold">Sintaxis forma 1:</font>
```java
type variable_name[] = new type[integer_expression];
```
<font style="color:green;font-weight: bold">Ejemplo forma 1:</font>
```java
// Declaración de array
String animales1[] = new String[3];

// Insertar valores
animales1[0] = "Gato";
```
<font style="color:orange;font-weight: bold">Sintaxis forma 2:</font>
```java
type[] variable_name = new type[integer_expression];
```
<font style="color:green;font-weight: bold">Ejemplo forma 2:</font>
```java
// Declaración de array
String[] animales2 = new String[3];

// Insertar valores
animales2[0] = "Leon";
```
## Utilizar palabra reservada new con inicializador
Cuenta con 2 posibles formas:
<font style="color:orange;font-weight: bold">Sintaxis forma 1:</font>
```java
type variable_name[] = new type[] {valores};
```
<font style="color:green;font-weight: bold">Ejemplo forma 1:</font>
```java
// Declaración de array
int numeros1[] = new int[] {1, 2, 3, 4, 5, 6};

// Leer los valores
for (int i = 0; i < numeros1.length; i++) {
	System.out.println(numeros1[i]);
}
```
<font style="color:orange;font-weight: bold">Sintaxis forma 2:</font>
```java
type[] variable_name = new type[] {valores};
```
<font style="color:green;font-weight: bold">Ejemplo forma 2:</font>
```java
// Declaración de array
int[] numeros2 = new int[] { 1, 2, 3, 4, 5, 6 };

// Leer los valores
for (int i = 0; i < numeros2.length; i++) {
	System.out.println(numeros2[i]);
}
```
# Declaración de array de dos dimensiones
- Los arrays de dos dimensiones también son conocidos como **tabla** o **matriz**.
![[618f2ed3-ac62-4532-b0ff-893c55b40e33.webp]]
## Solo con inicializador
- Cuenta con 2 posible formas:
<font style="color:orange;font-weight: bold">Sintaxis forma 1:</font>
```java
type variable_name[][] = {{valor1_fila1, valor2_fila1}, {valor1_fila2}, valor2_fila2}};
```
<font style="color:green;font-weight: bold">Ejemplo forma 1:</font>
```java
// Declaración de array
String capitales[][] = { { "Madrid", "Alicante" }, { "Lisboa", "Paris" }, { "Tallin", "Londres" } };

// Leer los valores
System.out.println("Índice" + "[0][1] = " + capitales[0][1]);
}

// Resultado en consola
Índice[0][1] = Alicante
```
<font style="color:orange;font-weight: bold">Sintaxis forma 2:</font>
```java
type[][] variable_name = {{valor1_fila1, valor2_fila1}, {valor1_fila2}, {valor2_fila2}};
```
<font style="color:green;font-weight: bold">Ejemplo forma 2:</font>
```java
// Declaración de array
String capitales[][] = { { "Madrid", "Alicante" }, { "Lisboa", "Paris" }, { "Tallin", "Londres" } };

// Leer los valores
System.out.println("Índice" + "[0][1] = " + capitales[0][1]);
}

// Resultado en consola
Índice[0][1] = Alicante
```
## Utilizar palabra reservada new sin inicializador.
- Cuenta con 2 posible formas:
<font style="color:orange;font-weight: bold">Sintaxis forma 1:</font>
```java
type variable_name[][] = new type[integer_expression][integer_expression];
```
<font style="color:orange;font-weight: bold">Sintaxis forma 1 irregular:</font>
```java
int numeroIrregular[][] = new int[3][]; // Se asignan 3 filas al array
numeroIrregular[0] = new int[2]; // Se asignan 2 columnas a la fila 0
```
<font style="color:green;font-weight: bold">Ejemplo forma 1:</font>
```java
// Declaración de array
String animales[][] = new String[2][2];

// Insertar valores
animales[0][0] = "Gato";
animales[0][1] = "Perro";
animales[1][0] = "Pájaro";
animales[1][1] = "Ratón";

// Leer los valores
System.out.println("Índice[1][0] = " + animales[1][0]);

// Resultado en consola
Índice[1][0] = Pájaro
```
<font style="color:orange;font-weight: bold">Sintaxis forma 2:</font>
```java
type[][] variable_name = new String[integer_expression][integer_expression];
```
<font style="color:green;font-weight: bold">Ejemplo forma 2:</font>
```java
// Declaración de array
String[][] animales2 = new String[2][2];

// Insertar valores
animales2[0][0] = "Gato";
animales2[0][1] = "Perro";
animales2[1][0] = "Pájaro";
animales2[1][1] = "Ratón";

// Leer los valores
System.out.println("Índice[1][0] = " + animales2[1][0]);

// Resultado en consola
Índice[1][0] = Pájaro
```
<font style="color:orange;font-weight: bold">Sintaxis forma 2 irregular:</font>
```java
int[][] numeroIrregular2 = new int[3][]; // Se asignan 3 filas al array
numeroIrregular2[0] = new int[2]; // Se asignan 2 columnas a la fila 0
```
<font style="color:salmon; font-weight:bold">Matrices irregulares:</font>
![[Captura de pantalla 2025-03-16 133623.png]]
## Utilizar palabra reservada new con inicializador
- Cuenta con 2 posible formas:
<font style="color:orange;font-weight: bold">Sintaxis forma 1:</font>
```java
type variable_name[][] = new type[][] { {"Fila1_Col1", "Fila1_Col2"}, {"Fila2_Col1", "Fila2_Col2"} };
```
<font style="color:green;font-weight: bold">Ejemplo forma 1:</font>
```java
// Declaración de array
String numeros1[][] = new String[][] { {"Fila1_Col1", "Fila1_Col2"}, {"Fila2_Col1", "Fila2_Col2"} };

// Leer los valores
System.out.println(numeros1[1][0]);

// Resultado en consola
Fila2_Col1
```
<font style="color:orange;font-weight: bold">Sintaxis forma 2:</font>
```java
type[][] variable_name = new type[][] { {"Fila1_Col1", "Fila1_Col2"}, {"Fila2_Col1", "Fila2_Col2"} };
```
<font style="color:green;font-weight: bold">Ejemplo forma 2:</font>
```java
// Declaración de array
String[][] numeros1 = new String[][] { {"Fila1_Col1", "Fila1_Col2"}, {"Fila2_Col1", "Fila2_Col2"} };

// Leer los valores
System.out.println(numeros1[1][0]);

// Resultado en consola
Fila2_Col1
```