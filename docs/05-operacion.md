# Guía de operación y mantenimiento

## Objetivo

Garantizar el correcto funcionamiento de la infraestructura mediante tareas periódicas de supervisión y mantenimiento.

## Tareas diarias

* Comprobar el estado de Apache.
* Verificar el estado de MariaDB.
* Revisar las métricas de Netdata.
* Comprobar la existencia de copias de seguridad recientes.

## Tareas semanales

* Revisar el espacio libre en disco.
* Comprobar los registros del sistema.
* Verificar el correcto funcionamiento del firewall.
* Revisar posibles actualizaciones disponibles.

## Tareas mensuales

* Aplicar actualizaciones de seguridad.
* Eliminar archivos innecesarios.
* Comprobar la restauración de las copias de seguridad.
* Revisar usuarios y permisos.

## Comandos útiles

Comprobar Apache:

```bash
sudo systemctl status apache2
```

Comprobar MariaDB:

```bash
sudo systemctl status mariadb
```

Comprobar el firewall:

```bash
sudo ufw status
```

Actualizar el sistema:

```bash
sudo apt update
sudo apt upgrade
```
## Buenas prácticas

* Mantener el sistema actualizado.
* Supervisar periódicamente los servicios.
* Realizar copias de seguridad frecuentes.
* Mantener una documentación actualizada.

## Mantenimiento del balanceador

Tareas recomendadas:

- Verificar el estado del servicio HAProxy.
- Revisar los logs de funcionamiento.
- Comprobar el reparto de carga entre servidores.
- Mantener el software actualizado.

Comprobar servicio:

bash
sudo systemctl status haproxy