**ARP**: Address Resolution Protocol - Protocolo de Resolución de Direcciones
	Este sirve para traducir direcciones IP a MAC. Cuando un dispositivo quiere enviar algo a cierta dirección IP pero no sabe la dirección MAC, lo que hace es enviar un mensaje de broadcast preguntando a todos los demás dispositivos quién tiene la dirección destino, cuando este mensaje le llega a la dirección destino, esta contesta con su dirección MAC haciendo que el dispositivo que envía la información ya sepa a dónde mandarla y agrega la dirección MAC a la trama de Ethernet.
	https://www.fortinet.com/resources/cyberglossary/what-is-arp

FTP: File Transfer Protocol - Protocolo de Transferencia de Datos
	Este se usa para transferir datos de una red basada en TCP, como el internet. Este funciona abriendo dos conexiones (por eso usa dos puertos bien conocidos) entre los dos clientes a comunicarse, una de estas se usa para comandos y respuestas entre estos, tales como "send", "get", "change directory" y "transfer".
	Este tiene tres modos, "block", "stream" y "compress"
		Stream: Hace que FTP maneje la información en una cadena de datos sin límites entre ellos.
		Block: Separa los datos en bloques.
		Compress: FTP usa un algoritmo llamado "Lempel-Ziv" para comprimir los datos.
	https://www.fortinet.com/resources/cyberglossary/file-transfer-protocol-ftp-meaning

SSH: Secure Shell - Shell Seguro - Protocolo SSH
	Este protocolo permite conexiones seguras mediante autenticación de llaves, credenciales como usuario y contraseña o passkey, además de criptografía. Consiste en un protocolo que verifica las conexiones mediante un cifrado asimétrico de llaves privada y pública, posterior suele haber un usuario y contraseña para acceder, y genera un cifrado simétrico para los paquetes que se envían mediante la red. 
	Tiene una infinidad de usos pero principalmente se usa para administraciones remotas, aun que debido a sus permisos de alto nivel puede considerarse un gran riesgo si se llegan a filtrar las llaves privadas.
	No tiene una capa específica en el modelo OSI pero muchos autores creen que es la 7.
	https://www.cloudflare.com/learning/access-management/what-is-ssh/

Telnet: Teletype Network - Protocolo Telnet
	Este es un protocolo similar a SSH, permite conexiones remotas a otros dispositivos mediante una interfaz únicamente de texto, las diferencias principales con SSH es que este es mucho más ligero lo que permite que sistemas con pocos recursos puedan funcionar hasta en múltiples conexiones en simultaneo de Telnet. Un problema que tiene es que no genera cifrado, por lo que las instrucciones e información que se transmite, se envía en texto plano, esto puede ser peligroso en redes abiertas al público en general ya que pueden robar la información con extrema facilidad.
	https://www.lenovo.com/us/en/glossary/what-is-telnet/

SMTP: Simple Mail Transfer Protocol - Servidor SMTP - Protocolo de Transferencia Simple de Correo
	Este es un protocolo que permite el envío de correos mediante la red, esto mediante la estandarización de un "sobre" que envuelva todos los datos a enviar, cabe aclarar que este protocolo solo envía el correo pero para poder verlo se utilizan otros protocolos separados. El funcionamiento es relativamente simple, revisa el encabezado del destino y si está en la misma red lo envía, si no, lo reenvía al servidor más cercano que tenga la dirección, y así sucesivamente hasta llegar al destino final.
	Para ver bien los correos debes usar un cliente de correos y protocolos POP o IMAP.
	https://www.cloudflare.com/learning/email-security/what-is-smtp/

DNS: Domain Name Server - Servidor de Nombres de Dominio
	

DHCP
HTTP
HTTPS
