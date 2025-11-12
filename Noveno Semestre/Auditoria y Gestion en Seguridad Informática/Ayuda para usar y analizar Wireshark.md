### Mi Flujo de Trabajo Recomendado (Resumen)

Cuando abras tu próximo archivo desconocido:

1. **NO FILTRES.** Ve a `Statistics > Protocol Hierarchy`. (Toma 10 segundos). Anota mentalmente los protocolos principales.
    
2. Ve a `Statistics > Conversations`. (Toma 15 segundos). Mira la pestaña `IPv4` y `TCP` y ordena por paquetes/bytes para ver quiénes son los "top talkers".
    
3. **FILTRA.** Empieza con los filtros de texto plano: `http`, `ftp`, `telnet`. Usa `Follow > TCP Stream` en cualquier cosa que parezca un login.
    
4. **FILTRA OTRA VEZ.** Busca anomalías: `tcp.flags.syn == 1`, `dns`, `arp`.
    

Ese proceso de 4 pasos te dirá el 90% de la historia que contiene el archivo.