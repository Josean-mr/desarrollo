# Instalación
## Docker engine
[Enlace](https://docs.docker.com/engine/install/)
- Comprobar instalación con comando:
	- docker run hello-world
## Permiso usuario Linux
- Nuevo usuario:
	- useradd -s /bin/bash -m -G docker *usuario*
- Usuario existente:
	- usermod -aG docker *usuario*
## Agregar contenedores
[Docker hub](https://hub.docker.com/)
## Comandos Docker
- Instalar contendedores:
	- docker run *nombre_imagen*
- Listar contenedores iniciados:
	- docker ps
- Listar todos los contenedores:
	- docker ps -a
- Eliminar contenedor:
	- docker rm *id_contenedor*
- Iniciar contenedor
	- docker start *id_contenedor*
- Detener contenedor:
	- docker stop *id_contenedor*
- Inspeccionar contenedor:
	- docker inspect *id_contenedor*
	- Ver IP:
		- docker inspect *id_contenedor* | grep IP
- Copiar fichero a contenedor:
	- docker cp *nombre*:*/ruta_destino/*
		- docker cp fichero.sql:/tmp/
- Ingresar a termina de contenedor
	- docker exec -it *id_contenedor* bash