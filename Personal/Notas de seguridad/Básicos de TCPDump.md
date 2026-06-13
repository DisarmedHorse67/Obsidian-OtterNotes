:~ tcpdump = Comando base (Si no se está en el usuario "root" es necesario el "sudo").
:~ tcpdump -r {Nombre del Archivo} = Muestra el archivo indicado.
:~ tcpdump < -v, -vv, -vvv> -r = Muestra más a detalle el archivo solicitado.
:~ -D = Muestra las interfaces disponibles.
:~ -i {Interfaz} = Para usar una interfaz en específico.
:~ src {ip-add}= Filtra por Origen.
:~ dst {ip-add}= Filtra por Destino.
:~ dst port {puerto} = Filtra por puerto.
:~ {protocolo} = Filtra por protocolo.
:~ {and} {or} = Se usan para encadenar comandos.
:~ -c = Limita el escaneo a cierto número de capturas.
:~ -n = Esta opción desactiva las traducciones de puertos y direcciones a nombres.
:~ -w {Nombre del Archivo} = Para guardar tu archivo .pcap.
:~ grep = Este se puede usar, incluidos muchos de sus parámetros, para buscar palabras específicas que contengan los paquetes.
:~ tcp[tcpflags] (== tcp-ack/tcp-syn/tcp-fin/tcp-push/tcp-urg/tcp-rst) = Estas sirven para filtrar por banderas tcp
:~ tcp[tcpflags] == 24 = Esto se usa para obtener más de una bandera a la vez, se suma en binario 
![[Pasted image 20260528154840.png]]
:~ ip [#] = este nos ayuda a dar más información de la ip, se puede buscar IP's específicas, o se puede buscar por encabezados específicos declarando el número del encabezado que se busca dentro de los corchetes, por ejemplo el 8 indica el TTL

El comando grep permite buscar texto específico:
-i no ve diferencia entre mayúsculas o minúsculas
-A muestra las líneas después de lo que se buscó
-B muestra las lineas antes de lo que se buscó