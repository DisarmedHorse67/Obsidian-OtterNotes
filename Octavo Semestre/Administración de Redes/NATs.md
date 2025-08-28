Estático == Una dirección interna a una externa
Dinámico == Una o varias internas a una o varias externas
PAT (Sobrecarga) == Una o muchas internas a una sola externa


Comandos:
Nat Estática
R2(config)# **ip nat inside source static 192.168.10.254 209.165.201.5**
R2(config)# **interface serial 0/1/0**
R2(config-if)# **ip address 192.168.1.2 255.255.255.252**
R2(config-if)# **ip nat inside**
R2(config-if)# **exit**
R2(config)# **interface serial 0/1/1**
R2(config-if)# **ip address 209.165.200.1 255.255.255.252**
R2(config-if)# **ip nat outside**

Nat Dinámica
cuando tenemos pool de direcciones, y en caso de tener más de 4k peticiones agregamos "overload"
ip nat pool <Nombre> <donde inicia> <donde termina>  netmask <mascara>
ip nat inside source list 1 pool <Nombre>

R2(config)# **ip nat pool NAT-POOL1 209.165.200.226 209.165.200.240 netmask 255.255.255.224**
R2(config)# **access-list 1 permit 192.168.0.0 0.0.255.255**
Router(config)# **ip nat inside source list** {_access-list-number_ | _access-list-name_} **pool** _pool-name_
R2(config-if)# **ip nat inside source list 1 pool NAT-POOL1**
R2(config)# **interface serial 0/1/0** R2(config-if)# **ip nat inside**
R2(config)# **interface serial 0/1/1** R2(config-if)# **ip nat outside**