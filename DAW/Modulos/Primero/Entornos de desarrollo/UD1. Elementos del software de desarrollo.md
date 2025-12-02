# 1. Introducción a los lenguajes de programación
Un programa informático es una serie de comandos ejecutados por el equipo que permiten obtener, modificar y mostrar información. Es decir, gestionar la información.
1. Se escribe el código a través de un <font style = "color:salmon">editor</font>.
2. Se traduce el programa escrito a lenguaje máquina. Proceso llamado <font style = "color:salmon">compilación</font>.
![[Captura de Pantalla 2024-10-03 a las 17.46.27.png]]
La compilación se realiza en 2 pasos:
1. El compilador transforma el código fuente en código objeto (lenguaje máquina).
2. El compilador llama a un editor de vínculos (enlazador o ensamblador) que permite insertar funciones y bibliotecas.
![[Captura de Pantalla 2024-10-03 a las 17.56.23.png]]
El resultado será un archivo ejecutable.
# 2. Tipos de lenguajes de programación
![[Captura de Pantalla 2024-10-03 a las 18.06.45.png]]
## <font style = "color:salmon">Según niveles</font>

| GENERACIÓN       | CARACTERÍSTICAS                                                                           | DEPENDEN DE LA MÁQUINA |
| ---------------- | ----------------------------------------------------------------------------------------- | ---------------------- |
| 1º generación 1G | Lenguaje máquina.                                                                         | Sí                     |
| 2º generación 2G | Lenguajes de programación de bajo nivel. Ensamblador.                                     | Sí                     |
| 3º generación 3G | Lenguajes de programación de alto nivel. FOR, WHILE, IF, etc.                             | Generalmente No        |
| 4º generación 4G | Mayoría de lenguajes con interfaz gráfica. Herramientas CASE de diseño de bases de datos. |                        |
| 5º generación 5G | Lenguajes naturales.                                                                      |                        |
## <font style = "color:salmon">Según paradigmas de programación</font>

| PARADIGMA                                                                                                                             | CARACTERÍSTICAS                                                                                                                                                           |
| ------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Programación <font style = "color:green">Imperativa</font>                                                                            | Los problemas se resuelven especificando una secuencia de acciones a realizar a través de funciones. Las sentencias modifican el estado del programa. Ejemplo: C, Pascal. |
| Programación <font style = "color:green">Orientada a Objetos</font> y<br>Programación <font style = "color:green">Estructurada</font> | Forman parte de la programación imperativa.                                                                                                                               |
| Programación <font style = "color:green">Declarativa</font>                                                                           | La solución se alcanza a través de mecanismos internos de control, no se especifica exactamente cómo llegar a ella.                                                       |
## <font style = "color:salmon">Según la forma en la que son ejecutados</font>

| TIPO DE LENGUAJE                                           | CARACTERÍSTICAS                                                                                                                   |
| ---------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| Lenguajes <font style = "color:green">compilados</font>    | Necesitan un programa traductor, llamado <font style = "color:salmon">compilador</font>.                                          |
| Lenguajes <font style = "color:green">interpretados</font> | No se genera el código objeto o máquina. Se va interpretando instrucción a instrucción.                                           |
| Lenguajes <font style = "color:green">virtuales</font>     | Es un código intermedio o <font style = "color:salmon">bytecode</font>, que puede ser interpretado una máquina virtual instalada. |
# 3. Compiladores y depuradores
## <font style = "color:salmon">Compiladores</font>
![[Pasted image 20241003203908.png]]
Un compilador es un programa que traduce un software escrito en un lenguaje de alto nivel, lenguaje de cuarta generación o de quinta generación, denominado programa fuente, en otro denominado programa objeto.
- La traducción de un compilador consta de 2 etapas:
	- <font style = "color:salmon">Etapa de análisis</font>:
		- <font style = "color:orange">Análisis léxico</font>:
			- Se localizan unidades básicas de información llamadas tokens.
			- Pasa por alto los comentarios.
		- <font style = "color:orange">Análisis sintáctico</font>:
			- Analiza que las estructuras están escritas en orden correcto.
			- Ejemplo:
				- Que en las asignaciones, el identificador aparezca a la izquierda del operador (de asignación).
		- <font style = "color:orange">Análisis semántico</font>:
			- Revisa el programa fuente tratar de encontrar errores semánticos.
			- Este tipo de errores se denominan advertencias o warnings.
	- <font style = "color:salmon">Etapa de síntesis</font>:
		- <font style = "color:orange">Generación de código intermedio</font>:
			- Es un código propio del compilador que permite la transportar el lenguaje a otros ordenadores.
		- <font style = "color:orange">Optimización del código</font>:
			- Es una optimización del código intermedio.
		- <font style = "color:orange">Generación del código</font>:
			- Generación del código final después de la optimización del código.
![[Pasted image 20241003204637.png]]
## <font style = "color:salmon">Depuradores</font>
Los depuradores facilitan la detección y, en muchos casos, la recuperación de errores producidos en las diferentes fases de la compilación.
# 4. Fases del desarrollo de una aplicación
![[Pasted image 20241004222315.png]]
## <font style = "color:salmon">1. Análisis</font>
- Es la etapa más importante en el desarrollo del software.
- Se establece el producto a desarrollar.
- Se requiere comunicación entre cliente y analista.
- Si falta información se puede recurrir al desarrollo de prototipos.
- Al final de la fase se han de tener claros las funcionalidades y requerimientos a desarrollar en la aplicación.
![[Pasted image 20241004222725.png]]
## <font style = "color:salmon">2. Diseño</font>
- Se alcanza con mayor precisión una solución óptima de la aplicación.
	- Recursos físicos y lógicos del sistema donde se ejecutará la aplicación.
![[Pasted image 20241004223014.png]]
## <font style = "color:salmon">3. Codificación</font>
- Creación y traducción del código fuente.
- Implica realizar pruebas de funcionamiento para comprobar que el software realiza las funciones programadas.
## <font style = "color:salmon">4. Pruebas</font>
- Pruebas para comprobar la calidad y estabilidad del programa.
![[Pasted image 20241004223521.png]]
- <font style = "color:#6976b5">Pruebas de unidad</font>:
	- Destinadas a la verificación de la menor unidad en el diseño del software (módulo).
- <font style = "color:#f2b33d">Pruebas de integración</font>:
	- Interconexión entre los módulos.
		- Puede ser **ascendente** o **descendente**:
			- Ascendente:
				- Comienza con la integración de los módulos de más bajo nivel.
			- Descendente:
				- Se construye primero el programa principal y se le van incorporando módulos conforme se van implementando.
- <font style = "color:#3bb273">Pruebas de sistema</font>:
	- Adaptar y ultimar detalles acerca del hardware.
	- Forzar errores.
	- Verificar mecanismo de protección y seguridad incorporados.
	- Pruebas de rendimiento.
	- Pruebas que pongan el sistema en situaciones anormales para evaluar estabilidad.
## <font style = "color:salmon">5. Explotación y mantenimiento</font>
- Explotación:
	- Es la implantación de la aplicación en el sistema o sistemas físicos donde van a funcionar habitualmente y su puesta en marcha para comprobar el buen funcionamiento.
	- Se facilita al cliente la documentación necesaria.
- Mantenimiento:
	- 3 tipos de mantenimiento:
		- <font style = "color:orange">Mantenimiento correctivo</font>:
			- Corregir errores no detectados en pruebas anteriores y que aparezcan con el uso normal de aplicación.
		- <font style = "color:orange">Mantenimiento adaptativo</font>:
			- Modificar el programa a causa de cambio de entorno gráfico y lógico. (Nuevas generaciones de ordenadores, versiones de SO, etc.)
		- <font style = "color:orange">Mantenimiento perfectivo</font>:
			- Mejorar sustancialmente la aplicación al recibir propuestas de los usuarios sobre nuevas posibilidades.
	- Los tipos <font style = "color:orange">adaptativo</font> y <font style = "color:orange">perfectivo</font> reinician el ciclo de vida, debiendo proceder de nuevo al desarrollo de cada una de sus fases para obtener un nuevo producto.
# 5. Documentación durante las fases del desarrollo
![[Pasted image 20241005110724.png]]
## <font style = "color:salmon">1. Documentación técnica</font>
- Documento donde queda reflejado:
	- El diseño del proyecto o aplicación.
	- La codificación de los programas.
	- Las pruebas realizadas para su correcto funcionamiento.
- Documento destinado a personal técnico en informática.
- Su principal objeto es facilitar el desarrollo, la corrección y el futuro mantenimiento.
## <font style = "color:salmon">2. Diseño</font>
- Documento donde queda reflejada la solución de la aplicación.
- Documento destinado a los programadores que van a desarrollar los programas de la aplicación.
- Su objetivo es que la codificación sea efectuada con la mayor calidad y rapidez posible.
## <font style = "color:salmon">3. Programa fuente</font>
- Ha de ser claro y legible.
- Seguir normas en el estilo de escritura. Como suficientes espacios para separar las expresiones o tabuladores para delimitar el ámbito de las estructuras de control.
## <font style = "color:salmon">4. Documentación de las pruebas</font>
- Especificar:
	- El tipo de prueba.
	- Módulos y programas para los que se efectúan dichas pruebas.
	- Datos de entrada.
	- Datos previstos de salida.
	- Datos reales obtenidos en las pruebas.
## <font style = "color:salmon">5. Guía de instalación</font>
- Es el documento que contiene la información necesaria para poner en marcha el sistema diseñado y para establecer las normas de explotación.
## <font style = "color:salmon">6. Guía de uso</font>
- La guía de uso o manual de usuario es el documento que contiene la información precisa y necesaria para que los usuarios utilicen correctamente los programas de la aplicación.
- Proviene de la guía técnica, pero se presenta de forma clara para el usuario.
## <font style = "color:green">Entregar un programa</font>
Cuando se entrega un programa se ha de entregar también:
- La documentación técnica.
- Los diagramas de diseño.
- El código fuente.
- La documentación de prueba.
- La guía de instalación.
- La guía de uso.
# 6. Metodologías ágiles
- Las metodologías ágiles son las que permiten adaptar la forma de trabajo a los condiciones del proyecto.
- Según el Manifiesto del desarrollo ágil de software, los equipos de desarrollo ágil deben valorar:
	- **Las personas y las interacciones** antes que los procesos y herramientas.
	- **El software en funcionamiento** antes que la documentación exhaustiva.
	- **La colaboración con el cliente** antes que la negociación contractual.
	- **La respuesta ante el cambio** antes que el apego a un plan.
## <font style = "color:salmon">SCRUM</font>
- Es la metodología ágil que más se usa.
- Su objetivo principal es satisfacer las necesidades del cliente mientras existe un entorno de comunicación, responsabilidad colectiva y progreso, transparente para el cliente.
- El proceso parte de una idea original que hay que ir construyendo, elaborando una lista de características que hay que ordenar por prioridad por la que el cliente quiere obtener el producto (producto backlog).
### <font style = "color:orange">Metodología SCRUM</font>
- Premia la aplicación de los 12 principios ágiles.
- Consiste en:
	- Ejecutar bloques temporales cortos y periódicos, llamados Sprints que suelen durar entre 2 y 4 semanas, que además es el plazo de retroalimentación y reflexión.
	- Cada Sprint es independiente, por lo que proporciona un resultado completo, que puede entregarse al cliente al finalizarlo.
	- El cliente prioriza los objetivos del proyecto.
- La metodología SCRUM aplicada a la construcción de software, se centra en tener claro que es lo que el cliente quiere, que es lo que NO quiere, y en el orden que lo quiere.
### <font style = "color:orange">Roles en SCRUM</font>
![[Pasted image 20241005121724.png]]
<font style = "color:orange">Scrum master</font>:
- Persona que dirige el proyecto.
- Se encarga de los problemas que puedan surgir en el proyecto.
- Está en comunicación con el Product owner.
- Mantiene al equipo al día en lo que se refiere a SCRUM:
	- Coaching.
	- Mentoring.
	- Formación.
<font style = "color:orange">Producto owner (PO)</font>:
- Persona más cercana a los clientes.
- Traslada al Product Backlog las tareas y las prioriza.
<font style = "color:orange">Team Members (Equipo)</font>:
- Resto de personal del equipo.
### <font style = "color:orange">Eventos en SCRUM</font>
![[Pasted image 20241005122258.png]]
<font style = "color:orange">1. Sprint</font>:
- Característica principal de la metodología SCRUM.
- Cuando se inicia un proyecto se divide en partes que deben tener un fin. A esas partes se les denomina Sprint.
<font style = "color:orange">2. Planificación del sprint</font>:
- Es la parte en que se define que y como se va a hacer en Sprint.
<font style = "color:orange">3. SCRUM diario</font>:
- Reunión diaria para ver el progreso y la tendencia que lleva el Sprint hasta su final generando un plan para las siguientes 24 horas.
<font style = "color:orange">4. Revisión del Sprint</font>:
- Responde a la pregunta ¿Qué se ha completado?, se verifica con respecto al backlog.
<font style = "color:orange">5. Retrospectiva del Sprint</font>:
- Reunión de equipo que revisa objetivos:
	- Que se han cumplido.
	- Que se ha hecho bien.
	- Que no se ha hecho tan bien.
- Para que errores cometidos no se repitan en futuros Sprints o proyectos.
### <font style = "color:orange">Artefactos de SCRUM</font>
Se conoce como artefactos de Scrum aquellos elementos que garantizan la transparencia de información para la toma de decisiones:
![[Pasted image 20241005124515.png]]
<font style = "color:orange">A. Product Backlog (PB)</font>:
- Se elabora con el cliente.
- Lista con los elementos necesarios para satisfacer las necesidades del cliente con el software.
- Se prioriza de más a menos importante para el cliente.
<font style = "color:orange">B. Sprint Backlog</font>:
- Elementos del Product Backlog que se seleccionan para realizar durante el sprint en el que se trabaja.
- Se establece la duración de cada Sprint.
- Para hacer visible el avance, se muestran en tableros llamados Tableros Scrum.
<font style = "color:orange">C. Incremento</font>:
- Cualquier elemento que se haya desarrollado durante el Sprint que se pondrá a disposición del usuario final en forma de Software.