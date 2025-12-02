# <font style="color:salmon">Refactorización</font>
## <font style="color:orange">Patrones más usuales</font>
### Extraer método:
- Es una manera sencilla para crear un nuevo método a partir de un fragmento de código de un miembro existente.
- <font style="color:green">Ejemplo</font>:
1. Código del programa:
```java
public class RefactorizacionExtraerMetodo {
	public static void main(String[] args) {
		
		String saludar;
		saludar = "Hola, te saludo.";
		System.out.println(saludar);
	}

}
	```
2. Seleccionamos el código a refactorizar y hacemos clic en "Extraer método":
![[Captura de Pantalla 2025-02-25 a las 18.02.23.png]]
3. Escribimos el nombre del método y se generará.
```java
public class RefactorizacionExtraerMetodo {

	public static void main(String[] args) {

		sumar();

}

private static void sumar() {
	String saludar;
	saludar = "Hola, te saludo.";
	System.out.println(saludar);

	}

}
```
### Métodos en línea:
- Los **métodos en línea** es una técnica común utilizada en programación, siendo una aplicación directa de la definición de refactoring en cuanto a la optimización de código cambiando su estructura interna sin afectar su funcionalidad. El caso específico del método en línea se presenta cuando se tiene uno o más métodos cuyos códigos son lo suficientemente auto-explicativos como para poder prescindir de ellos. Bastará con sustituir las llamadas al método por el cuerpo de dicho método.
[ Ejemplos de refactorización](https://recacha.wordpress.com/2012/08/16/refactoring-en-eclipse-2-inline-method/)
# Control de versiones
## <font style="color:salmon">Tipos</font>: Centralizados y distribuidos
### Centralizados.
- Repositorio de fuentes:
	- Es el directorio único en el que están almacenadas las fuentes y sus versiones.
- Servidor:
- Es cuando las fuentes y sus versiones están almacenados en un **único directorio** (repositorio de fuentes) de un ordenador (servidor).
### Distribuidos.
- No hay repositorio central.
- Todos los desarrolladores tienen su copia del repositorio con todas sus versiones.
- <font style="color:green">Ejemplos</font>:
	- Git.
	- Mercurial.
### En la nube.
- Es un repositorio que funciona teniendo un perfil en un servidor externo.
## <font style="color:salmon">Herramientas</font>
- El sistema de control de versiones se puede realizar de forma manual, pero se aconseja utilizar los **VCS** (Version Control System).
- **Conceptos** sobre la estructura general:
	- **Repositorio**: es el lugar centralizado donde se almacena todo el historial de versiones del código fuente. Puede ser centralizado (como en SVN) o distribuido (como en Git y Mercurial). Contiene ramas (branches) que representan líneas independientes de desarrollo.
	- **Ramas (Branches)**: son líneas de desarrollo independientes dentro del repositorio. La rama principal suele llamarse "master" o "main". Los desarrolladores pueden crear ramas para trabajar en nuevas características o solucionar problemas sin afectar la rama principal.
	- **Commit**: es un conjunto de cambios realizados en el código. Cada commit tiene un mensaje descriptivo que explica los cambios realizados. Los commits están asociados con un autor y una marca de tiempo.
	- **Clonación (Clone)**: permite a los desarrolladores copiar un repositorio completo en sus propias máquinas locales para trabajar de forma independiente. Es útil para trabajar sin conexión a Internet y para facilitar la colaboración.
	- **Fusión (Merge)**: combina cambios de una rama en otra. Puede ocurrir cuando se completa una nueva característica o se soluciona un problema en una rama de desarrollo y se fusiona con la rama principal.
	- **Trazabilidad (Log)**: mantiene un registro detallado de todos los commits realizados en el repositorio. Facilita la identificación de quién realizó qué cambios y cuándo.
	- **Etiquetas (Tags)**: se utilizan para marcar puntos específicos en la historia del repositorio, como versiones lanzadas. Proporcionan un identificador fijo para referenciar fácilmente un estado específico del código.
	- **Conflictos**: cuando dos ramas modifican la misma parte del código, puede surgir un conflicto. Los desarrolladores deben resolver estos conflictos antes de fusionar las ramas.
### CVS
![[Pasted image 20250225195101.png]]
- Fue el primer sistema de control de versiones de código abierto con acceso a redes.
- CVS sólo versiona ficheros, no directorio.
- No soporta cambios atómicos.
### Subversion
- Escrito para reemplazar a CVS.
### SVK
- Construido sobre Subversion.
- Permite desarrollo distribuido, cambios locales, mezcla sofisticada de cambios y la habilidad de reflejar/clonar árboles desde sistemas de control de versiones que no son SVK.
### Mercurial
- Ofrece una completa indexación cruzada de ficheros y conjunto de cambios.
### GIT
- Producto llevado a cabo por Linus Trovalds para manejar el árbol fuente del kernel de Linux.
- Cada directorio de trabajo de GIT es un repositorio completo con plenas capacidades de gestión de revisiones, sin depender del acceso a la red o de un servidor central.
### Bazaar
- Cuenta con modelo de repositorio central y distribuido.
- Proporciona servicios de alojamiento gratuito a través de los sitios web LaunchPad y SourceForge.
### GitHub
[web](https://docs.github.com/es)
[Tutorial de Git y GitHub](https://youtu.be/jSJ8xhKtfP4?si=TvAoQ_x77uCRa59a)
- La web utiliza el sistema de control de versiones GIT.
- La plataforma también hace de red social conectando desarrolladores con usuarios.
- La combinación de Git, para ordenador personal, y GitHub, para compartir en la nube con otras personas el proyecto, es lo que más se suele usar en las empresas.
## <font style="color:salmon">Repositorios</font>
![[Pasted image 20250225200440.png]]
# Documentación
## <font style="color:salmon">Pasos</font>
![[Pasted image 20250225200747.png]]
## <font style="color:salmon">Uso de comentarios</font>
- Durante la fase de implementación es necesario comentar convenientemente cada una de las partes del programa.
### Herramientas alternativas.
- Word.
- Sharepoint.
- Adobe FrameMaker: para archivos de texto largo y complejos.
#### Gestión documental con software libre.
- Nuxeo.
- Alfresco.