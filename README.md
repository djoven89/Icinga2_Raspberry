# Icinga2 sobre una Raspberry PI

El objetivo de este repositorio es configurar un stack de monitorización listo para implementar en producción en menos de 30 minutos de forma totalmente desatendida en una Raspberry Pi o un servidor con Ubuntu Server 20.04.

El stack de monitorización lo conforman los siguientes servicios:

* **Icinga2:** Basado en Nagios, es el software que se encargará de monitizar el estado de los servidores y servicios configurados.

* **Icingaweb2:** Panel gráfico de administración que permite analizar el estado de los servidores y servicios configurados, además, también permite realizar cierto tipo de gestiones sobre los objetos monitorizados.

* **Mysql:** Servicio encargado de almacenar y gestionar las bases de datos que requiere tanto Icinga2 como Icingaweb2.

* **Apache:** Servicio web que sobre el que se configura el panel gráfico Icingaweb2.

* **PHP:** Lenguaje de programación necesario para ejecutar Icingaweb2.

* **InfluxDB:** Base de datos basada en series de tiempo sobre los que se almacenarán las métricas obtenidas por Icinga2.

* **Grafana:** Software de visualización que permite crear gráficas con las métricas obtenidas por Icinga2 y almacenadas en Influxdb.

El resto de roles desarrolladores son:

* **system:** Se encarga de realizar ciertas configuraciones básicas sobre el sistema.

* **logs:** Modifica el comportamiento de los logs más importes del sistema.

* **ssh:** Aplica ciertas configuraciones de seguridad sobre el servicio.

* **firewall:** Mediante ufw se encarga de añadir una capa de seguridad extra sobre el servidor.

* **fail2ban:** Software encargado de evitar intentos de ataque basados en fuerza bruta.

Mencionar también que los servicios web han sido configurados para que trabajen únicamente sobre HTTPS. Además, se han añadido distintas políticas de seguridad sobre cada rol con la finalidad de proporcionar una mayor robusted sobre el servidor y los servicios que lo conforman.


&nbsp;
## Requisitos

A continuación se indican los requisitos que hay que cumplir para poder usar este repositorio:

* Tener instalado Ansible en un equipo para la realización del despliegue del stack de monitorización.

* Tener instalada Ubuntu Server 20.04 en la Raspberry Pi o en un servidor físico o virtual.

* El servidor Ubuntu Server 20.4 deberá ser accesible vía SSH desde el equipo donde está instalado Ansible, además, deberá tener conexión a Internet para la descarga de los distintos paquetes que conforman el stack de monitorización.


&nbsp;
## Variables

Cada rol tiene definidas unas series de variables que permiten customizar la configuración del servicio, como por ejemplo, las credenciales de las bases de datos usadas para los distintos servicios o los puertos que se usan. Para más información sobre las variables establecidas y una breve descripción, leer el archivo '**README.md**' del rol en cuestion.

Comentar también que en el directorio '**host_vars**' hay una plantilla en la cual están definidas todas las variables establecidas y que son requeridas para el despliegue.


&nbsp;
## Despliegue

A continuación se explican los pasos a realizar para desplegar el stack de monitorización desarrollado.


1. [Instalación](https://raspberryparatorpes.net/sistemas-operativos/ubuntu-20-04-lts-para-raspberry-pi/) de Ubuntu Server 20 en la Raspberry o en un equipo físico o virtual.

2. Configuración de red sobre el servidor.

3. [Instalación](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html) de Ansible en el equipo desde el cual desplegaremos el stack de monitorización usando Ansible.

4. Desde el equipo sobre el que se ha instalado Ansible. nos cercioraremos de que podemos conectarnos vía SSH.

5. Clonamos el repositorio en el equipo desde el que lanzaremos el playbook de Ansible.

```
https://github.com/djoven89/Icinga2_Raspberry.git
```

6. Copiamos el archivo '**hosts-plantilla**':

```
cp -v hosts-plantilla hosts
```

7. Editamos el archivo y establecemos la dirección IP del servidor donde se instalará el stack de monitorización.

8. Copiamos el archivo '**ansible.cfg-plantilla**':

```
ansible.cfg-plantilla ansible.cfg
```

9. Lo editamos y establecemos las credenciales de acceso al servidor donde se instalará el stack de monitorización.

10. Copiamos el archivo '**host_vars/server-plantilla**' y lo llamamos igual que el FQDN que tendrá el servidor.

```
cp -v host_vars/server-plantilla host_vars/monitoring.icecrown.lan
```

11. Lo editamos y establecemos el valor deseado para las variables.

12. Una vez que hayamos terminado de definir la configuración de Ansible, procederemos a comprobar la conexión vía SSH contra el servidor:

```
ansible -m ping server
```

**NOTA:** Si el comando arroja cualquier error, habrá que comprobar la conectividad y la configuración definida en los pasos: **7**, **9** y **11**.

13. A continuación, ejecutamos el playbook para la el despliegue del stack de monitorización sobre el servidor:

```
ansible-playbook deploy_icinga2.yaml
```

**NOTA:** En caso de que alguna tarea falle y el playbook se detenga, es posible volver a ejecutar la tarea en la que falló usando el párametro `--start-at-task="Nombre_de_la_tarea_que_falló"`.


&nbsp;
## Molecule

Cada rol tiene configurado un directorio llamado '**molecule**' el cual permite comprobar la estabilidad del rol ante cambios del código o actualizaciones de los servicios.

La configuración definida está basada en el entorno de pruebas que uso normalmente, el cual está formado por VirtualBox 6.1 y Vagrant 2.2.9.


&nbsp;
## Enlaces

Algunos enlaces interesantes que he usado para el desarrollo a nivel general del proyecto.

### Sintáxis

* https://docs.ansible.com/ansible-lint/rules/default_rules.html
* https://yamllint.readthedocs.io/en/stable/rules.html
* https://www.jeffgeerling.com/blog/2020/ansible-101-jeff-geerling-youtube-streaming-series#e07

### Software

* https://molecule.readthedocs.io/en/latest/
* https://www.jeffgeerling.com/blog/2020/ansible-101-jeff-geerling-youtube-streaming-series#e08

