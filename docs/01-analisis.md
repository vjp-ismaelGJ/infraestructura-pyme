# Análisis de requisitos

## Introducción

Una pequeña empresa necesita desplegar una infraestructura informática que permita alojar su página web corporativa y un sistema de gestión interna. El objetivo es disponer de una plataforma segura, estable y fácilmente administrable.

## Objetivos del proyecto

* Implementar una infraestructura basada en tecnología LAMP.
* Permitir el acceso seguro a los servidores mediante SSH.
* Disponer de una base de datos para la aplicación web.
* Disponer de una base de datos independiente para la gestión interna.
* Implementar mecanismos de monitorización.
* Diseñar una estrategia de copias de seguridad y recuperación ante desastres.

## Requisitos funcionales

### Servidor web

* Servidor Apache.
* Soporte para PHP.
* Capacidad para alojar aplicaciones web dinámicas.

### Base de datos

* Motor MariaDB o MySQL.
* Base de datos para la página web.
* Base de datos independiente para la gestión interna.

### Administración remota

* Acceso mediante SSH.
* Restricción de acceso mediante firewall.

### Monitorización

* Supervisión del uso de CPU.
* Supervisión del uso de memoria RAM.
* Supervisión del almacenamiento.
* Supervisión del tráfico de red.

### Copias de seguridad

* Backup automático de las bases de datos.
* Backup automático de archivos importantes.
* Política de retención de copias.

## Requisitos no funcionales

* Seguridad.
* Disponibilidad.
* Mantenibilidad.
* Escalabilidad básica.
* Facilidad de recuperación ante fallos.
