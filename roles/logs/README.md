# Rol: logs

Este rol configurará el servicio de logrotate para rotar de forma personalizada los archivos de log del sistema principales.


## Variables que contiene el rol 'logs'

| Variable | Valor por defecto | Descripción |
|----------|-------------------|-------------|
| logs_rotated_dir | /var/log/logs_rotated/ | Directorio donde se almacenarán los archivos de log rotados |
| logs_rotation_daily | 180 | Número de veces que rotarán los logs diariamente (syslog, auth.log, kernel.log) |
| logs_rotation_weekly | 48 | Número de veces que rotarán los logs semanalmente (dpkg.log, apt/history.log, apt/term.log) |
| logs_max_size | 100M | Tamaño máximo que tendrá un archivo de log |


## Enlaces

* https://www.freedesktop.org/software/systemd/man/journald.conf.html
