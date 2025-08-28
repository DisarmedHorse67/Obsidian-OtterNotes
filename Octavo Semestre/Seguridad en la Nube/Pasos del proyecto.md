PfSense
* generar 3 vSwitches en esxi, y agregarlos a portgroups
* Instalar PfSense y configurar dichos switches
* Configurar las reglas para permitir acceso entre las redes
BD y WebServer
* Configurar la interfaz de red desde los archivos (en este caso en /etc/netplan/50-cloud-init.yaml)

* dentro de la bd configurar el ssh para acceso remoto 
* dentro de bd configurar los tupos de usuario con acceso a la base de datos con respectivos permisos
BD
* configurar la base de datos
* agregar el comando sudo mysql_secure_installation
WebServer
* dentro de web server descargar y activar el apache
* Solucionar problemas de apache
