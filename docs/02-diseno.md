# Diseño de la infraestructura

## Arquitectura general

La infraestructura propuesta se basa en una arquitectura LAMP compuesta por un servidor Linux que aloja Apache, PHP y MariaDB. Además, se incorporan mecanismos de acceso remoto seguro, monitorización y copias de seguridad.

## Diagrama de la infraestructura

```text
                    Internet
                        |
                 Puerto 80/443
                        |
                +---------------+
                | Apache + PHP  |
                +---------------+
                        |
                Puerto 3306
                        |
                +---------------+
                |   MariaDB     |
                +---------------+

Administración remota:
SSH (Puerto 22)

Monitorización:
Netdata

Backups:
mysqldump + rsync
```

## Componentes software

| Componente    | Versión propuesta  | Función                       |
| ------------- | ------------------ | ----------------------------- |
| Ubuntu Server | 22.04 LTS          | Sistema operativo             |
| Apache        | 2.4.62             | Servidor web                  |
| PHP           | 8.2                | Ejecución de aplicaciones web |
| MariaDB       | 10.11              | Base de datos                 |
| Netdata       | Última estable     | Monitorización                |
| UFW           | Incluido en Ubuntu | Firewall                      |
| OpenSSH       | Última estable     | Administración remota         |

## Puertos utilizados

| Puerto | Protocolo | Servicio |
| ------ | --------- | -------- |
| 22     | TCP       | SSH      |
| 80     | TCP       | HTTP     |
| 443    | TCP       | HTTPS    |
| 3306   | TCP       | MariaDB  |

## Medidas de seguridad

* Acceso remoto mediante SSH.
* Uso de firewall UFW.
* Restricción de puertos abiertos.
* Separación lógica entre servicios.
* Estrategia de copias de seguridad periódicas.
