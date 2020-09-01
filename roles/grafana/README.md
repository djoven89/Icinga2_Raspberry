# Rol: grafana

Este rol instalará y configurará Grafana, el cual permitirá crear gráficos con los valores almacenados en InfluxDB procedentes de Icinga2.


## Pendiente

* La tarea 'Terminando de customizar la configuración del servicio' no realiza cambio alguno. ¿Expresión regular del parámetro 'after'?


## Variables que contiene el rol

| Variable | Valor por defecto | Descripción |
|----------|-------------------|-------------|
| grafana_port | 20300 | Puerto de acceso a la interfaz gráfica de Grafana |
| grafana_log_rotation | 180 | Número de días máximo en los que repotará el log |
| grafana_admin | grafadmin | Nombre del usuario administrador de Grafana |
| grafana_admin_password | Graf@min2020! | Contraseña del usuario administrador de Grafana |
| grafana_datasource_name | datasource-influxdb | Nombre del datasource |
| influxdb_port | 8806 | Puerto del servicio InfluxDB |


## Enlaces

* https://grafana.com/docs/grafana/latest/administration/configuration/
* https://grafana.com/docs/grafana/latest/administration/configuration/
* https://grafana.com/docs/grafana/latest/administration/provisioning/
