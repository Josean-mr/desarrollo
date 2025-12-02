# 1. Entornos de desarrollo
- Los entornos de desarrollo están formados por un conjunto de software que facilitan o automatizan las actividades de desarrollo.
## <font style="color:salmon">1.1 Herramientas CASE.</font>
- Siglas de "<font style="color:#08F">Computer Aided Software Engineering</font>" -> Ingeniería de Software Asistida por Ordenador.
- <font style="color:green">Ejemplos</font> de uso:
	- Representar el modelo Entidad Relación de una base de datos, y extraer automáticamente de dicho modelo la documentación correspondiente al diccionario de datos.
### <font style="color:orange">1.1.1 Objetivos.</font>
![[76d0eaea-63e5-4793-9063-5d6e9ac00c93.webp]]
### <font style="color:orange">1.1.2 Estructura.</font>
- Elementos de una herramienta CASE:
![[bf3461c3-8c18-46fe-abc2-fed8daac109f.webp]]

### <font style="color:orange">1.1.3 Repositorio.</font>
- Es la <font style="color:#08F">base de datos central de una herramienta CASE</font>.
- Características importantes de un repositorio:
	![[Pasted image 20241206143304.png]]

### <font style="color:orange">1.1.4 Clasificación.</font>
![[174bbf85-f690-4146-b71f-74ee92340003.webp]]
Tipos más comunes de herramientas CASE:
![[Pasted image 20241206143535.png]]
- **Herramientas de análisis y diseño:**
	- Principal objetivo: Ayudar a la definición de requisitos del sistema y sus propiedades.
	- Permiten editar: Diagramas E/R, diagramas de flujo de datos, diagramas de clases, etc.
- **Herramientas de Generación de código y documentación:**
	- A partir de las especificaciones de diseño se puede generar código.
- **Herramientas de gestión de configuración:**
	- Herramienta capaz de gestionar la configuración de los sistemas.
		- Capacidades:
			- **Control de versiones:**
				- Proporciona almacenamiento y acceso controlado.
				- Registra cambios.
				- Permite recuperar versiones anteriores.
			- **Trazabilidad de requisitos:**
				- Permiten que un requisito pueda ser rastreado hasta su implementación.
			- **Análisis de impacto:**
				- Permite conocer los elementos del sistema que se ven afectados ante el cambio.
- **Herramientas de Prueba:**
	- CAST (Computer aided Software Testing) son desarrollos especialmente recientes dentro de la tecnología CASE.
	- Funcionalidades:
		![[Pasted image 20241206223506.png]]
- **Herramientas de Ingeniería Inversa:**
	- Objetivo es obtener información a partir de un producto, para determinar cómo fue fabricado.
	- Tareas que se llevan a cabo:
		- **Ingeniería inversa de datos**, capaces de extraer información del código fuente que describe la estructura de los datos, por ejemplo, construyendo diagramas E/R partiendo de un modelo de datos ya implementado.
		- **Ingeniería inversa de procesos**, a partir del código permiten aislar la lógica de las entidades y las reglas de negocio.
		- **Reestructuración de código fuente**, modifican su formato o implantan un formato estándar.
		- **Análisis de código**, cuyas funcionalidades van desde la tabulación automática del código fuente, hasta la posibilidad de ir visualizando dinámicamente las llamadas del mismo.
## <font style="color:salmon">1.2 Entornos de Programación.</font>
- Son las herramientas CASE que se encargan de dar soporte al desarrollador para la creación del código de los programas.
	![[Pasted image 20241206143950.png]]
	- **Entornos orientados al lenguaje:**
		- Entornos específicos a un lenguaje en particular.
	- **Entornos orientados a estructuras:**
		- Son como los orientados al lenguaje, pero además tienen un editor de estructura o editor sintáctico.
	- **Entornos basados en combinación de herramientas (Toolkit):**
		- Presentan una integración débil, fáciles de ampliar y adaptar a nuevas herramientas.
		- Presentan al desarrollador un conjunto de herramientas de modo que son capaces de interoperar entre ellas.
	- **Entornos multilenguaje:**
		- Para crear aplicaciones que combinan el código fuente en distintos lenguajes de programación:
			![[86efe910-f625-44c4-acf3-8bc8811b1654.png]]
### <font style="color:orange">1.2.1 Entornos profesionales más usados.</font>
![[Pasted image 20241206151819.png]]
## <font style="color:salmon">1.3 Ejemplos de Herramientas CASE.</font>
### <font style="color:orange">1.3.1 Microsoft Porject.</font>
Microsoft Project es un software de administración de proyectos para asistir a administradores de proyectos en el desarrollo de planificaciones, asignación de recursos a tareas, dar seguimiento al progreso, administrar presupuesto y analizar cargas de trabajo.

La aplicación puede crear un calendario de rutas críticas, y reconocer diferentes clases de usuarios, los cuales pueden contar con distintos niveles de acceso a proyectos, vistas y otros datos. Los objetos personalizables como calendarios, vistas, tablas, filtros y campos son almacenados en un servidor que comparte la información a todos los usuarios.
![[fd352d7c-73dd-440e-858e-0988558347b1.webp]]
### <font style="color:orange">1.3.2 Oracle JDeveloper</font>
Es un entorno integrado que cubre todo el ciclo de vida de desarrollo de software e integra distintas tecnologías utilizadas para la construcción de aplicaciones empresariales estándar. Sus principales características son:
	![[Pasted image 20241206152547.png]]
![[d5035161-967c-4022-9b68-4017723b2ddf.webp]]

