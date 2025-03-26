Estático == Una dirección interna a una externa
Dinámico == Una o varias internas a una o varias externas
PAT (Sobrecarga) == Una o muchas internas a una sola externa


Comandos:
cuando tenemos pool de direcciones, y en caso de tener más de 4k peticiones agregamos "overload"
ip nat pool <Nombre> <donde inicia> <donde termina>  netmask <mascara>
ip nat inside source list 1 pool <Nombre>
