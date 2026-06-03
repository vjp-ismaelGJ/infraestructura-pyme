# Monitorización del sistema

## Objetivo

La monitorización permite supervisar el estado de la infraestructura para detectar incidencias, cuellos de botella y posibles fallos antes de que afecten al servicio.

## Herramienta seleccionada

Se utilizará *Netdata*, una herramienta de monitorización en tiempo real que proporciona información detallada sobre el rendimiento del sistema mediante una interfaz web intuitiva.

## Métricas monitorizadas

### Recursos del sistema

* Uso de CPU.
* Uso de memoria RAM.
* Espacio disponible en disco.
* Carga del sistema.

### Servicios

* Estado del servidor Apache.
* Estado de MariaDB.
* Conectividad de red.

### Tráfico de red

* Tráfico entrante.
* Tráfico saliente.
* Velocidad de transferencia.

## Instalación propuesta

bash
sudo apt update
sudo apt install netdata

### Puerto utilizado

Netdata utiliza por defecto el puerto 19999/TCP para el acceso a la interfaz web de monitorización
## Acceso a la interfaz

Una vez instalado, Netdata estará disponible mediante navegador web:

text
http://IP_SERVIDOR:19999


## Beneficios

* Detección temprana de problemas.
* Supervisión en tiempo real.
* Visualización gráfica de métricas.
* Facilita las tareas de administración y mantenimiento.