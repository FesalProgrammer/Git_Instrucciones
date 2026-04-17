# GUIA INICIO DE REPO EN GITHUB ENLAZADO A ARCHIVO LOCAL

1. Crear carpeta local
2. Abrir carpeta con vsc
3. Crear archivo dentro de la carpeta local
4. Abrir GitHub y crear repo, para ello hay que hacer click en el simbolo (+).
5. Dar un nombre al repo (la carpeta en la nube de GitHub se llama repo), no tiene que ser el mismo de la carpeta creada de forma local pero si lo es no pasa nada. Lo mejor es que compartan el mismo nombre asi es mas facil parear nombre repository Git con nombre carpeta local.
6. Dejar la configuracion tal como esta y hacer click en "create repository".
7. Abrir la terminal del vsc y escribir: git init
8. git add .
9. git commit -m "primer commit"
   Luego escribe estas 3 lineas:
10. git remote add origin <https://github.com/FesalProgrammer/nombreDelRepo.git>
11. git branch -M main
12. git push -u origin main
    Listo.

# GUIA UNDOING CHANGES

Como Git registra todo lo que creas/escribes, puedes usar git restore mas el nombre del archivo y su extension para borrar lo ultimo escrito.
usar git restore --staged notas_git.md para restaurar un archivo que tiene un add a el estado anterior.
Usar git clean -xdf para borrar un archivo nuevo (untracked) que no ha sido registrado por git.
Si tienes un archivo que ya salio de untracked entonces usas git checkout para descartar lo ultimo. git checkout file name para ser especifico o git checkout . para descartar todo lo nuevo.
Si el archivo ya subio al stage entonces aqui no funciona git clean -xdf ni git checkout. Git te da una pista para bajarlo del stage usando git reset HEAD <file>
reglas que aplican para undoing un archivo ya commiteado, git reset --hard HEAD^ file lo elimina. git reset --softHEAD~1 lo baja al stage, un nivel y git --mixed HEAD~1 lo baja desde stage hasta el file system (un nivel).

# GUIA DE COMANDOS GIT

El flujo típico para registrar y compartir cambios:

1. Editás archivos en tu proyecto.
2. git add . "agrega cambios al área de preparación".
3. git commit -m "". crea un snapshot en el historial.
4. git push envía los commits al repositorio remoto.
   Creación de repositorios
   ● git init: convierte la carpeta actual en un repositorio Git local.
   ● git clone URL_DEL_REPOSITORIO: descarga una copia de un repositorio remoto.
   Comandos básicos
   ● git add archivo.txt
   ● git commit -m "Descripción breve del cambio"
   ● git push origin main
   ○ origin: nombre por defecto del repositorio remoto.
   ○ main: rama principal (antes master).
   Ramas (branches) y fusiones (merges)
   Las ramas permiten trabajar en nuevas funcionalidades sin afectar la rama principal.
   git branch nueva-funcionalidad # crea rama
   git checkout nueva-funcionalidad # cambia a la rama

# trabajás...

git add .
git commit -m "Implementar nueva funcionalidad"
git checkout main
git checkout <nombre de la branch> sirve para cambiar de rama
git merge nueva-funcionalidad # fusiona cambios
git branch -d nueva-funcionalidad # elimina rama local
Colaboración en proyectos mediante GitHub
GitHub es un servicio que aloja repositorios remotos y facilita la colaboración:
● Fork: copia personal de un repositorio para trabajar independientemente.
● Pull Request (PR): propuesta de cambios al repositorio original.
● Revisiones de código: comentarios y discusión antes de fusionar.
Buenas prácticas de versionado
● Mensajes de commit claros: usar infinitivo y describir el cambio (p.ej., Agregar función dividir).
● Commits pequeños y frecuentes: facilitan revertir y entender el historial.
● Uso de ramas: mantener main estable, desarrollar en ramas separadas y fusionar cuando estén listas.
● Modelos de branching: adoptar Git Flow, GitHub Flow o similares para orden y consistencia.

# GUIA TAG COMMITS

Mark commits with tags
. git tag ver1

View tags
. git tag -list

Push
. git push --tags

Check it out
. git checkout ver1

# GUIA STASH (salvar tu trabajo que no esta listo para ser commiteado)

Save working directory
. git stash save "description"

View stashes
. git stash list

Bring them back
. git stash pop (and remove from stash)
. git stash apply (leave in stash)

Remove
. git stash drop (clear)

# GUIA REMOTE

Las operaciones basicas del trabajo remote son: Push (repositorio local hacia repositorio remoto) y Fetch(desde el reppositorio remoto hacia el repositorio local)

Add
. git remote add <name> <url>
. git remote add origin git@github.com:user/repo.git

View
. git remote -v
. git remote show <name>

tip: when copy a command line in gitbash, use ctrl + insert for copying
tip: si se pierde el repositorio local, para restaurarlo debes crear otro repositorio en github con el mismo nombre del repositorio local perdido y acompañado de la palabra backup al final del nombre.
Copiar la url que te da github y abrir gitbash. escribir "git remote remove origin". Luego escribbir "git remote -v". luego escribes "git remote add origin <pegar aqui la url previamente copiada>". Luego escribir "git remote -v" para chequear que la nueva url haya sido salvada en github. Entoces corremos el comando git push y luego seguimos las instrucciones de gitbash, es decir, corremos el siguiente comando: git push --set-upstream origin master. git log para ver que el push ha sido hecho.
