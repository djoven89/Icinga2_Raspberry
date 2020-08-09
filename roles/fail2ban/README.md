# Rol: fail2ban

Este rol instalará y configurará el servicio Fail2Ban, el cual nos proporcionará una capa más de seguridad frente a autenticaciones fallidas como al servicio SSH.


## Variables que contiene el rol

| Variable | Valor por defecto | Descripción |
|----------|-------------------|-------------|
| ssh_port | 2201 | Puerto del servicio SSH |
| ban_tries | 4 | Número de intentos máximo antes de bloquear la IP |
| ban_time | 5m | Tiempo en minutos en los que estarán bloqueados las IPs |
| logs_rotated_dir | /var/log/logs_rotated/ | Directorio donde se almacenarán los archivos de log rotados |
| logs_rotation | 180 | Número de veces que rotarán el log 'fail2ban.log' |
| logs_max_size | 100M | Tamaño máximo que tendrá un archivo de log |


## Enlaces

