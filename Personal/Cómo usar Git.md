Si se va a usar la misma cuenta siempre "inicia sesión"
$ git config --global user.email "tu_email@example.com"
$ git config --global user.name "Tu Nombre"
$ git config --global --list (Puedes verificar aquí si se configuró correctamente)

Agrega el repo a tu git
$ git remote add origin https://github.com/tu-usuario/tu-repositorio.git

Agregas lo que vas a meter (en este caso todo con ".") y haces el commit
$ git add .
$ git commit -m "Primer commit: Subida inicial de mi bóveda Obsidian"

Por último lo pusheas 
$ git push -u origin main