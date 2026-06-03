# Instalación y configuración de la base de datos

## Objetivo

Proporcionar almacenamiento persistente para la aplicación web y el sistema de gestión interno.

## Instalación de MariaDB

bash
sudo apt install mariadb-server


Comprobar el estado del servicio:

bash
sudo systemctl status mariadb


## Configuración inicial

bash
sudo mysql_secure_installation


## Creación de bases de datos

Base de datos para la web:

sql
CREATE DATABASE web_empresa;


Base de datos para la gestión interna:

sql
CREATE DATABASE gestion_interna;


## Creación de usuarios

sql
CREATE USER 'usuario_web'@'localhost' IDENTIFIED BY 'password_seguro';
GRANT ALL PRIVILEGES ON web_empresa.* TO 'usuario_web'@'localhost';

CREATE USER 'usuario_gestion'@'localhost' IDENTIFIED BY 'password_seguro';
GRANT ALL PRIVILEGES ON gestion_interna.* TO 'usuario_gestion'@'localhost';

FLUSH PRIVILEGES;


## Servicios implicados

* MariaDB 10.11
* Cliente MySQL

## Recomendaciones

* Utilizar contraseñas robustas.
* Limitar privilegios a los usuarios.
* Realizar copias de seguridad periódicas.