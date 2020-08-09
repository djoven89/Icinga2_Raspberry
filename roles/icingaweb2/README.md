# Rol: icingaweb2

Este rol instalará y configurará el servicio Icingaweb2, el cual nos permitirá tener una interfaz de administración gráfica para ver el estado de los servidores monitorizados.


## Consideraciones

* Para obtener el hash de la contraseña de la variable '**icingaweb2_user_password**' se tiene que ejecutar el comando:

```
openssl passwd -1 Icing@_2020!
```


## Variables que contiene el rol

| Variable | Valor por defecto | Descripción |
|----------|-------------------|-------------|
| db_port | 33006 | Puerto de la base de datos |
| db_user | dbaroot | Nombre de usuario de la base de datos |
| db_user_password | db@_2020! | Contraseña del usuario de la base de datos |
| db_icinga2 | db_icinga2 | Nombre de la base de datos de Icinga2 |
| db_icinga2_user | dba_icinga2 | Nombre del usuario administrador de la base de datos de Icinga2 |
| db_icinga2_user_password | Db@_Icinga2! | Contraseña del usuario administrador de la base de datos de Icinga2 |
| db_icingaweb2 | db_icingaweb2 | Nombre de la base de Icingaweb2 |
| db_icingaweb2_user | dba_icinga2 | Nombre del usuario administrador de la base de datos de Icinga2 |
| db_icingaweb2_user_password | Db@_Icinga2! | Contraseña del usuario administrador de la base de datos de Icinga2 |
| api_port | 5665 | Puerto de la API de Icinga2 |
| api_user | icingapi | Nombre del usuario de la API de Icinga2 |
| api_user_password | Icing@CmD! | Contraseña del usuario de la API de Icinga2 |
| icingaweb2_user | icingadmin | Nombre del usuario de la interfaz gráfica de Icingaweb2 |
| icingaweb2_user_password | $1$H0epSDUH$u.K5sW0tpnphYyICj55Oy/ | Contraseña del usuario de la interfaz gráfica de Icingaweb2 |
| site_domain | icinga.icecrown.lan | Nombre del dominio en el cual escuchará Apache |
| site_short_name | icinga | Nombre del subdominio |
| site_path | /srv/apache/test | Directorio donde se alojará el sitio web |
| site_cert_file | /etc/ssl/certs/ssl-cert-snakeoil.pem | Ruta al certificado para el dominio |
| site_cert_key | /etc/ssl/private/ssl-cert-snakeoil.key | Ruta a la clave del certificado para el dominio |


## Enlaces

