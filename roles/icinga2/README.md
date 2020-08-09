# Rol: icinga2

Este rol instalará y configurará el servicio Icinga2.


## Variables que contiene el rol

| Variable | Valor por defecto | Descripción |
|----------|-------------------|-------------|
| db_user | dbaroot | Usuario de la base de datos que creará la base de datos y el usuario de la base de datos de Icinga2 |
| db_user_password | db@_2020! | Contraseña del usuario de la base de datos que creará la base de datos y el usuario de la base de datos de Icinga2 |
| db_icinga2 | db_icinga2 | Nombre de la base de datos de Icinga2 |
| db_icinga2_user | dba_icinga2 | Nombre del usuario administrador de la base de datos de Icinga2 |
| db_icinga2_user_password | Db@_Icinga2! | Contraseña del usuario administrador de la base de datos de Icinga2 |
| logs_rotated_dir | /var/log/logs_rotated/ | Directorio donde se almacenarán los archivos de log rotados |
| logs_rotation | 180 | Número de veces que rotarán el log 'ufw.log' |
| logs_max_size | 100M | Tamaño máximo que tendrá un archivo de log |


## Enlaces

