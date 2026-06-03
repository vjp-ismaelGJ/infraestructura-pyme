# Instalación y configuración del servidor web

## Objetivo

Implementar un servidor web basado en Apache con soporte para aplicaciones PHP.

## Actualización del sistema

bash
sudo apt update
sudo apt upgrade


## Instalación de Apache

bash
sudo apt install apache2


Comprobar el estado del servicio:

bash
sudo systemctl status apache2


## Instalación de PHP

bash
sudo apt install php libapache2-mod-php


Comprobar la versión instalada:

bash
php -v


## Reinicio del servicio Apache

bash
sudo systemctl restart apache2


## Comprobación de funcionamiento

Acceder desde un navegador a:

text
http://IP_SERVIDOR


Si aparece la página por defecto de Apache, la instalación se ha realizado correctamente.

## Servicios implicados

* Apache 2.4
* PHP 8.2

## Buenas prácticas

* Mantener el sistema actualizado.
* Utilizar HTTPS en producción.
* Restringir servicios innecesarios.

## Configuración del balanceador HAProxy

Se utilizará HAProxy como balanceador de carga situado delante del servidor Apache.

Instalación:

bash
sudo apt install haproxy


Comprobar servicio:

bash
sudo systemctl status haproxy


Funciones principales:

- Distribución del tráfico HTTP y HTTPS.
- Mejora de la disponibilidad.
- Posibilidad de ampliar la infraestructura con varios servidores web.