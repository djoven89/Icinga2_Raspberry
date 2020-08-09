# Rol: ssh

Este rol securizará el servicio de SSH.


## Variables que contiene el rol

| Variable | Valor por defecto | Descripción |
|----------|-------------------|-------------|
| ssh_port | 2201 | Puerto para el servicio SSH |
| ssh_tries | 6 | Número de intentos máximos permitidos antes de cerrar la sesión de autenticación |
| ssh_grace | 120 | Tiempo máximo en segundos para establecer las credenciales durante el login |
| ssh_sessions | 4 | Número máximo de conexiones SSH permitidas |
| ssh_alive | 600 | Tiempo máximo en segundos de inactividad al estar conectado por SSH |


## Enlaces

