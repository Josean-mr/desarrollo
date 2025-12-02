# 1. Placas base. Formatos
## <font style = "color:salmon">ATX</font>
- El más utilizado.
- Llegó en 1995.
- Dimensiones: 305x244 mm:
## <font style = "color:salmon">MicroATX</font>
- Versión más compacta de la ATX.
- Destaca su uso en gaming.
- Dimensiones: 244x244 mm.
## <font style = "color:salmon">Mini-ITX</font>
- Creadas en 2001.
- Para escritorios de pequeño compacto.
- Limita la utilización de expansiones.
- Dimensiones: 170x170 mm.
## <font style = "color:salmon">E-ATX</font>
- Orientadas a estaciones de trabajo y servidores.
- Soportan un mayor número de componentes.
- Dimensiones: 305x330 mm.
# 2. Estructura y componentes
Un Sistema Informático es un conjunto de elementos que interactúan entre sí con el fin de llevar a cabo el tratamiento de la información de forma automática.
## <font style = "color:salmon">Elementos de un sistema informático</font>
![[Pasted image 20241007183454.png]]
<font style = "color:orange">Hardware</font>:
- La parte física del computador.
- Se clasifica en:
	- CPU:
		- Núcleo del sistema.
		- Conta de placa base, el procesador y la memoria principal (RAM).
		- Contiene:
			- Conjunto de registros:
				- Espacio donde se almacena de manera temporal los datos e instrucciones dentro del procesador.
			- Unidad aritmético-lógica:
				- Es lo que forma el conjunto de operaciones aritméticas y lógicas con los datos que han sido almacenados en el procesador.
			- Unidad de control:
				- Encargada de controlar el funcionamiento de los componentes del procesador.
		- Memoria interna:
			- Nivel 0. Registros:
				- Se almacenan los datos sobre los que trabajan directamente desde la unidad de control.
			- Nivel 1. Caché:
				- Memoria compuesta por lo circuitos integrados SRAM. Tiene como función controlar los accesos a la memoria principal para que sean los menos posibles.
			- Nivel 2. Memoria principal:
				- Formada por la DRAM. Tiene como función el almacenamiento de instrucciones y datos que se utilizan en los procesos.
		![[Pasted image 20241007190251.png]]
		- Interfaces de entrada/salida.
			- Son circuitos que se encargan de la comunicación entre la unidad central y los procesos.
			- Formas de operar:
				- Por consulta:
					- La CPU va chequeando de forma periódica.
				- Por interrupciones:
					- El dispositivo es el encargado de establecer el momento de la transferencia de datos.
				- Por acceso directo a memoria (DMA):
					- El dispositivo puede operar directamente sobre la memoria. La CPU debe haber concedido permiso.
		- Discos:
			- Son dispositivos magnéticos o mecánicos que se utilizan para el almacenamiento de datos de modo no volátil.
			- Tipos de interfaces.
				- ATA/IDE.
				- SCSI.
				- SATA.
				- Conexiones externas.
	- Periféricos:
		- Son los dispositivos mediante los cuales el ordenador central se comunica con el exterior.
		- Clasificación:
			- De entrada:
				- Teclado.
				- Ratón.
				- Escáner.
			- De salida:
				- Monitor.
				- Altavoz.
			- De E/S:
				- Módem.
				- Adaptador o tarjeta de red.
		- Plug&Play:
			- Los periféricos se instalan de forma automática.

<font style = "color:orange">Software</font>:
- Conjunto de programas le dan vida al Hardware.
- Se clasifica en:
	- Firmware:
		- Conjunto de instrucciones necesarias para el buen funcionamiento del computador.
		- También llamado "Programa de arranque".
	- Sistema Operativo:
		- Conjunto de programas que administra dispositivos y recursos del computador.
	- Aplicaciones:
		- Programas que realizan tareas específicas de interés para el usuario.
<font style = "color:orange">Usuarios</font>:
- Personas que utilizan la computadora:
- Se clasifican en:
	- Desarrolladores:
		- Personas que utilizan la computadora para crear hardware o software.
	- Técnicos:
		- Personas encargadas de instalar y dar mantenimiento al hardware o al software.
	- Operarios:
		- Los usuarios finales que utilizan el computador como ayuda para sus actividades cotidianas.
# 3. Montaje de equipos
- El principal problema suele ser la electricidad estática.
	- Nuestro cuerpo puede acumular carga estática de hasta 4.000 voltios.
	- Se recomienda utilizar pulsera antiestática que se debe unir al chasis del equipo.
	- Se recomienda utilizar bolsas plateadas ESD.
## <font style = "color:salmon">Ergonomía</font>
- Iluminación apropiada.
- Máquinas con distancia de separación suficiente.
- Postura de trabajo:
![[Pasted image 20241007192037.png]]
## <font style = "color:salmon">Normas de protección ambiental</font>
Reciclaje de material informático:
- Punto de reciclado.
- Devolverlo a los distribuidores.
- Donarlo a una ONG.
# 4. Características de las redes. Ventajas e inconvenientes
# 5. Tipos de redes
## <font style = "color:salmon">Características de las redes</font>
### <font style = "color:orange">Redes dedicadas o exclusivas.</font>
![[Pasted image 20241007193618.png]]
### <font style = "color:orange">Redes compartidas.</font>
- Son las que reúnen un gran número de usuarios.
- Las más utilizadas son las:
	- Redes de conmutación de paquetes:
		- Los nodos regulan el tráfico de paquetes.
	- Redes de conmutación de circuitos:
		- Los centros de conmutación establecen un circuito dedicado entre dos estaciones que se comunican.
### <font style = "color:orange">Según propiedad de la red.</font>
- Redes privadas:
	- Redes gestionadas por particulares, empresas u organizaciones.
	- Sólo tienen acceso los terminales propietarios.
- Redes públicas:
	- Perteneces a organismos estatales.
### <font style = "color:orange">Según alcance o extensión geográfica.</font>
- WAN:
	- Wide Area Network.
- MAN:
	- Metropolitan Area Network.
- LAN:
	- Local Area Network.
# 6. Componentes de una red informática
## <font style = "color:salmon">Hardware</font>
![[Pasted image 20241007201009.png]]
### <font style = "color:orange">Dispositivos finales.</font>
- Servidor.
- Estación de trabajo.
- Tarjetas con Interfaz de red.
### <font style = "color:orange">Dispositivos intermedios.</font>
También denominados <font style = "color:salmon">equipos de conectividad</font>.
- Repetidor.
- Concentrador (Hub).
- Puente (Bridge).
- Conmutador (Switch).
- Dispositivo de enrutamiento (Router).
- Pasarela (Gateway).
### <font style = "color:orange">Medios de transmisión.</font>
- Guiados:
	- Alámbricos
		- Par Trenzado:
			- Son dos hilos de cobre trenzado, aislados de forma independiente para reducir las interferencias electromagnéticas.
			- 2 tipos:
				- UTP:
					- Sin recubrimiento metálico.
				- STP:
					- Con recubrimiento metálico que evita interferencias externas.
		- Cable Coaxial:
			- Hilo conductor de cobre envuelto por una malla metálica.
		- Fibra óptica:
			- Señal transmitida a través de la luz.
			- 2 tipos:
				- Monomodo:
					- La luz no rebota en las paredes.
					- Mayor velocidad y distancia.
					- Más cara.
				- Multimodo:
					- Más de un haz de luz.
- No guiados:
	- Inalámbricos:
		- Microondas:
			- Requiere línea de visión de directa.
		- Infrarrojos:
			- Emisión/recepción de un haz de luz.
		- Wifi:
			- Estándar para redes locales.
		- Bluetooth:
			- Solo permite la conexión directa entre 2 dispositivos.
# 7. Topologías de red
La topología de red es la forma en que se distribuyen los diferentes sistemas que la componen.
![[Pasted image 20241007202757.png]]
## <font style = "color:salmon">Topología en bus</font>
- Forma más simple de conectar una red.
- Las computadoras comparten una sola línea compartiendo el mismo canal de datos.
- Si un equipo falla, la red se ve afectada.
![[Pasted image 20241007203557.png]]
## <font style = "color:salmon">Topología en anillo</font>
- Las computadoras se unen en un circuito cerrado formado por un anillo en el que la información circula en una dirección.
- Una variante es la topología de doble anillo, que añade un segundo anillo redundante.
![[Pasted image 20241007224620.png]]
## <font style = "color:salmon">Topología en estrella</font>
- Los equipos se conectan a un dispositivo central (normalmente un hub o swtich) que gestiona las comunicaciones.
- El fallo de uno de los equipos no paraliza el resto de la red.
- Es el más utilizado de los tres.
![[Pasted image 20241007224842.png]]
## <font style = "color:salmon">Topología en malla</font>
- Relativa inmunidad a congestiones en el cableado y por avería.
- Posibilidad de orientar el tráfico por caminos alternativos si un nodo está averiado u ocupado.
![[Pasted image 20241007225828.png]]
# 9. Mapa físico y lógico de una red local
![[Pasted image 20241007225409.png]]

