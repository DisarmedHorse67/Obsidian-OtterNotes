Configurar máquinas virtuales
* Instalación base de 3 máquinas virtuales en VMware, un kali linux, Debian y Windows Server, todos se quedan con configuraciónes básicas.
* Configuración de adaptadores en Host-Only en todas las máquinas para contar únicamente con conexión entre estas.
Kali
* Este será el "atacante" o "scanner" desde donde realizaremos los comandos de nmap
Comandos usados
* netdiscover
Este comando lo usamos para descubrir qué redes se encuentra dentro de la red por medio del protocolo arp
* nmap
	* -O
	* -sV
	* --script vuln
	* --script auth
	* -p-
	* -sS
	* -Pn
