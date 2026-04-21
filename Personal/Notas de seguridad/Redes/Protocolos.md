**ARP**: Protocolo de Resolución de Direcciones
	Este sirve para traducir direcciones IP a MAC. Cuando un dispositivo quiere enviar algo a cierta dirección IP pero no sabe la dirección MAC, lo que hace es enviar un mensaje de broadcast preguntando a todos los demás dispositivos quién tiene la dirección destino, cuando este mensaje le llega a la dirección destino, esta contesta con su dirección MAC haciendo que el dispositivo que envía la información ya sepa a dónde mandarla y agrega la dirección MAC a la trama de Ethernet.

FTP: Protocolo de Transferencia de Datos
	Este se usa para transferir datos de una red basada en TCP, como el internet. Este funciona abriendo dos conexiones (por eso usa dos puertos bien conocidos) entre los dos clientes a comunicarse, una de estas se usa para comandos y respuestas entre estos, tales como "send", "get", "change directory" y "transfer".
	Este tiene tres modos, "block", "stream" y "compress"
		Stream: Hace que FTP maneje la información en una cadena de datos sin límites entre ellos.
		Block: Separa los datos en bloques.
		Compress: FTP usa un algoritmo llamado "Lempel-Ziv" para comprimir los datos.
SSH
Telnet
SMTP
DNS
DHCP
HTTP
HTTPS
