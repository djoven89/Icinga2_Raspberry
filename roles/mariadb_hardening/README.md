# Rol: mariadb_hardening

Este rol securizará el servicio MariaDB.


## Pendiente

* Usar el módulo 'listen_ports_facts' para obtener la disponibilidad del puerto de la base de datos.
* Buscar los usuarios sin contraseñas.
* Cambiar el plugin de autenticación a los usuarios que usen 'auth_socket'.


## Variables que contiene el rol

| Variable | Valor por defecto | Descripción |
|----------|-------------------|-------------|
| db_user | root | Usuario de la base de datos que hará las acciones en el rol |
| db_user_password | db@_2020! | Contraseña del usuario de la base de datos que hará las acciones en el rol |
| db_root_rename | dbaroot | Nombre del usuario de la base de datos que tendrá 'root' tras ser renombrado |
| db_data | /opt/mariadb | Directorio de datos del servicio MariaDB |
| db_remote_access | false | Permite el acceso a MariaDB desde redes externas |


## Enlaces

