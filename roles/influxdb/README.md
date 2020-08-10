# Rol: influxdb

Este rol instalará y configurará InfluxDB, el objetivo será que los valores obtenidos por Icinga2 los almacene en la base de datos de InfluxDB para que después, Grafana los muestre en forma de gráfica.


## Variables que contiene el rol

| Variable | Valor por defecto | Descripción |
|----------|-------------------|-------------|
| influxdb_port | 8086 | Puerto del servicio InfluxDB |
| influxdb_db | db_influx | Base de datos donde se almacenerá la información monitorizada de Icinga2 |
| influxdb_admin | influxdba | Usuario administrador de InfluxDB |
| influxdb_admin_password | InfluxDb@2020! | Contraseña del usuario administrador de InfluxDB |
| influxdb_user | influxicinga | Usuario de InfluxDB que gestionará la base de datos de monitorización |
| influxdb_user_password | InfluxIcing@2020! | Contraseña del usuario de la base de datos de monitorización |

## Enlaces

* https://docs.influxdata.com/influxdb/v1.8/administration/authentication_and_authorization/#set-up-authentication
* https://docs.influxdata.com/influxdb/v1.8/administration/authentication_and_authorization/#user-management-commands