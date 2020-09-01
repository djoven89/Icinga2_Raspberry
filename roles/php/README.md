# Rol: php

Este rol instalará y configurará el servicio PHP, el cual es necesario para Icingaweb2.

## Pendiente

* Revisar cómo se rotaría los logs de PHP.


## Consideraciones

* Icingaweb2 recomienda usar PHP 7.x, aunque todavía no es compatible todavía con PHP 7.4.


## Variables que contiene el rol

| Variable | Valor por defecto | Descripción |
|----------|-------------------|-------------|
| php_version | 7.3 | Versión de PHP que usará Icingaweb2 |
| server_timezone | Europe/Madrid | Zona horaria del servidor |
| logs_rotated_dir | /var/log/logs_rotated/ | Directorio donde se almacenarán los archivos de log rotados |
| logs_rotation_weekly | 48 | Número de veces que rotarán el log 'php_error.log' |
| logs_max_size | 100M | Tamaño máximo que tendrá un archivo de log |
