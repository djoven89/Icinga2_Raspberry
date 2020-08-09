# Rol: Firewall

Este rol configurará el firewall del servidor usando 'ufw'.


## Variables que contiene el rol

| Variable | Valor por defecto | Descripción |
|----------|-------------------|-------------|
| ssh_port | 2201 | Puerto para el servicio SSH |
| logs_rotated_dir | /var/log/logs_rotated/ | Directorio donde se almacenarán los archivos de log rotados |
| logs_rotation | 180 | Número de veces que rotarán el log 'ufw.log' |
| logs_max_size | 100M | Tamaño máximo que tendrá un archivo de log |


## Enlaces

