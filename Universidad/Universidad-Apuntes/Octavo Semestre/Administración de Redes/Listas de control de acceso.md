w100 a 199 - es extendida, permite declarar un origen, protocolo, destino.
1 a 99 - numeradas o estandar que solo toman dirección de origen
nombradas no cuentan con número, se agrega ip al inicio y el nombre al final.
Se crean en configuración global pero se deben aplicar a las interfaces pertinentes.
ACL extendidas se colocan cerca del origen.
ACL estándar se colocan cerca del destino.
Las listas cuentan con un denegar todo implícito, siempre y cuando la lista comience con un denegar, esta se tiene que modificar
Se debe configurar una regla de permitir al menos para no bloquear toda la comunicación.

Comandos.
ACL por número
access-list 100 remark RED 10 NO 30 :) == Para nombrar la regla
access-list 100 deny ip 192.168.10.0 0.0.0.255 192.168.30.0 0.0.0.255 == creación de regla 
access-list 100 permit ip 192.168.10.0 0.0.0.255 any == regla para permitir acceso a todo lo demás
Do show acc == para mostrar las listas
ip access-group 100 in == para agregar la lista a la interfaz

ACL por nombre
R1(config)#ip access-list extended 10NO30
R1(config-ext-nacl)#deny ip 192.168.10.0 0.0.0.255 192.168.30.0 0.0.0.255
R1(config-ext-nacl)#permit tcp 192.168.11.0 0.0.0.255 host 192.168.10.3 eq www == Si quieres poner por http
Router(config-ext-nacl)#permit tcp host 192.168.30.2 host 200.200.200.2 eq 443 == Si quieres que solo se comunique por https (no hay protocolo pero sí puerto)
R1(config-ext-nacl)#int g0/0
R1(config-if)#ip access-group 10NO30 in


