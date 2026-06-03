# Política de copias de seguridad

## Objetivo

Garantizar la recuperación de la información ante fallos del sistema, errores humanos o pérdidas de datos.

## Estrategia de copias de seguridad

Se realizará una copia automática diaria de:

* Bases de datos.
* Archivos de configuración.
* Documentación del proyecto.

## Copias de seguridad de bases de datos

Las bases de datos se respaldarán mediante la herramienta mysqldump.

Ejemplo:

bash
mysqldump -u root -p nombre_bd > backup.sql


## Copias de seguridad de archivos

Los archivos se copiarán utilizando rsync.

Ejemplo:

bash
rsync -av /origen /destino


## Automatización

Las copias se programarán mediante tareas cron.

Ejemplo:

bash
0 2 * * * /ruta/script_backup.sh


La ejecución se realizará diariamente a las 02:00.

## Retención de copias

* Copias diarias durante 7 días.
* Copias semanales durante 4 semanas.
* Eliminación automática de copias antiguas.

## Recuperación

En caso de incidencia, las copias permitirán restaurar:

* Bases de datos.
* Archivos de configuración.
* Información necesaria para la recuperación del servicio.