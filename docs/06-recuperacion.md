# Plan de recuperación ante desastres

## Objetivo

Restaurar el funcionamiento del sistema en caso de fallo crítico o pérdida de datos.

## Situaciones contempladas

* Fallo del servidor web.
* Corrupción de la base de datos.
* Eliminación accidental de archivos.
* Problemas de hardware.
* Errores de configuración.

## Recuperación del servidor web

Reinstalar Apache:

```bash
sudo apt install apache2
```

Restaurar los archivos de configuración y reiniciar el servicio:

```bash
sudo systemctl restart apache2
```

## Recuperación de bases de datos

Restaurar una copia de seguridad:

```bash
mysql -u root -p nombre_bd < backup.sql
```

## Recuperación de archivos

Restaurar archivos mediante rsync:

```bash
rsync -av /backup /destino
```

## Prioridades de recuperación

1. Recuperar la conectividad del servidor.
2. Restaurar la base de datos.
3. Recuperar la aplicación web.
4. Comprobar el correcto funcionamiento del sistema.

## Recomendaciones

* Verificar periódicamente las copias de seguridad.
* Documentar todas las incidencias.
* Mantener procedimientos de recuperación actualizados.
