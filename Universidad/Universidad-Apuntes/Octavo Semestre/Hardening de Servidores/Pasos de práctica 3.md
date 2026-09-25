Se realiza escaneo con nikto al puerto 80, se detectó que faltan las cabeceras 
* - Falta `X-Frame-Options` (riesgo de **clickjacking**).
- Falta `X-Content-Type-Options` (riesgo de **MIME sniffing**).
Realizamos **curl -I http://<IP> y observamos que no existen por el momento.

Los archivos de '/wp-links-opml.php`, `readme.txt` están expuestos, lo que revelan la versión de wordpress y algunos plugins, al probarlos descubrimos que sí están expuestos, la versión de wordpress instalada es 6.7.2

