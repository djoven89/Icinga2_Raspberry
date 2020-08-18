# Rol: apache

Este rol instalrá y configurará el servicio Apache2 requerido para Icingaweb2.


## Variables que contiene el rol

| Variable | Valor por defecto | Descripción |
|----------|-------------------|-------------|
| site_domain | icinga.icecrown.lan | Nombre del dominio en el cual escuchará Apache |
| site_short_name | icinga | Nombre del subdominio |
| site_path | /srv/apache/test | Directorio donde se alojará el sitio web |
| site_cert_file | /etc/ssl/certs/ssl-cert-snakeoil.pem | Ruta al certificado para el dominio |
| site_cert_key | /etc/ssl/private/ssl-cert-snakeoil.key | Ruta a la clave del certificado para el dominio |
| logs_rotated_dir | /var/log/logs_rotated/ | Directorio donde se almacenarán los archivos de log rotados |
| logs_rotation_daily | 180 | Número de veces que rotarán el log 'apache2/' |
| logs_max_size | 100M | Tamaño máximo que tendrá un archivo de log |


## Molecule

Funciona correctamente usando como provider Vagrant.


## Enlaces

