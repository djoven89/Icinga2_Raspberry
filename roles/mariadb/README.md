# Rol: mariadb

Este rol instalará y configurará el servicio MariaDB, el cual se usará para las bases de datos que requiere: Icinga2 e Icingaweb2.


## Variables que contiene el rol

| Variable | Valor por defecto | Descripción |
|----------|-------------------|-------------|
| db_root_password | db@_2020! | Contraseña del usuario de bases de datos 'root' |
| db_port | 33006 | Puerto para el servicio MariaDB |
| db_remote_access | false | Permite el acceso a MariaDB desde redes externas |
| db_query | false | Aplica algunos parámetros de configuración referentes a las consultas SQL |
| logs_rotated_dir | /var/log/logs_rotated/ | Directorio donde se almacenarán los archivos de log rotados |
| logs_rotation_daily | 180 | Número de veces que rotarán los logs diariamente (error.log) |
| logs_rotation_weekly | 48 | Número de veces que rotarán los logs semanalmente (mariadb_general.log, mariadb_slow.log) |
| logs_max_size | 100M | Tamaño máximo que tendrá un archivo de log |


## Enlaces

