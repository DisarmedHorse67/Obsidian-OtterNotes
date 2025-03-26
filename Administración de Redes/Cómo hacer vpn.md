R1(config)#interface tunnel 0
R1(config-if)#ip add 44.44.44.1 255.255.255.252 
R1(config-if)#no shut
R1(config-if)#tunnel source se0/0/0
R1(config-if)#tunnel destination 2.2.2.2
R1(config-if)#tunnel mode gre ip (En la vida real se usa IPsec pero packet tracer no soporta esto)

Se crea en ambos extremos, ambos tuneles tienen que ser el mismo número para lograr conexión.