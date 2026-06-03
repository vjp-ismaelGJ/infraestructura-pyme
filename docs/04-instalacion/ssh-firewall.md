# Configuración de SSH y firewall

## Objetivo

Permitir la administración remota del servidor de forma segura y controlar el acceso a los servicios mediante UFW.

## Instalación de OpenSSH

bash
sudo apt install openssh-server


Comprobar el servicio:

bash
sudo systemctl status ssh


## Instalación de UFW

bash
sudo apt install ufw


## Configuración básica del firewall

Permitir acceso SSH:

bash
sudo ufw allow 22/tcp


Permitir tráfico HTTP:

bash
sudo ufw allow 80/tcp


Permitir tráfico HTTPS:

bash
sudo ufw allow 443/tcp


Activar el firewall:

bash
sudo ufw enable


Comprobar reglas activas:

bash
sudo ufw status


## Recomendaciones de seguridad

* Deshabilitar el acceso SSH del usuario root.
* Utilizar autenticación mediante claves SSH.
* Mantener OpenSSH actualizado.
* Limitar el número de puertos abiertos.

## Puertos utilizados

| Puerto | Servicio |
| ------ | -------- |
| 22     | SSH      |
| 80     | HTTP     |
| 443    | HTTPS    |