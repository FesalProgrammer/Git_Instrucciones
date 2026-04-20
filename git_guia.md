# GUIA INICIO DE REPO EN GITHUB ENLAZADO A ARCHIVO LOCAL
Metodo 1
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

Metodo 2
1. Ya creadas e instaladas las 2 SSH (publica y privada), crear repositorio en github.



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

LA INSTALACION DE LAS SSH SE REALIZA EN GITBASH (ES EL INTERPRETE DEL KERNEL DE UNIX PARA WINDOWS). EN MAC Y LINUX SE TRABAJA DIRECTAMENTE EN LA TERMINAL


Para abrir gitbash:
1. click simbolo window y escribir git, hacer click en gitbash
2. Tambien se puede hacer en la terminal al lado del simbolo + hacer click y seleccionar gitbash de la lista desplegada.

Checking for existing SSH keys
Before you generate an SSH key, you can check to see if you have any existing SSH keys.

Open Git Bash.
Para abrir gitbash:
1. click simbolo window y escribir git, hacer click en gitbash
2. Tambien se puede abrir VSC y abrir una NEW TERMINAL y  al lado del simbolo + (en la terminal) hacer click y seleccionar gitbash de la lista desplegada(si es que esta instalado, sino habria que instalar GIT).

texto ejemplo de la terminal gitbash:
fesal@LAPTOP-MD2LE27A MINGW64 ~
$
verificar que el path termina exactamente en el nombre de usuario.

Enter ls -al ~/.ssh to see if existing SSH keys are present.

$ ls -al ~/.ssh #copiar y pegar este codigo en gitbash (no incluir simbolo $)

PARA SALIR (logout) DE GITBASH => EXIT
PARA LIMPIAR DE GITBASH => CLEAR

SI TE ENCUENTRAS EN EL DIRECTORIO INICIAL: fesal@LAPTOP-MD2LE27A MINGW64 ~

PARA CAMBIAR AL ESCRITORIO => cd Desktop/
fesal@LAPTOP-MD2LE27A MINGW64 ~/Desktop


# Lists the files in your .ssh directory, if they exist

Para conocer tu usuario y el correo que tienes configurado en git usa:
git config --list

user.name=FesalProgrammer
user.email=FesalProgramming@gmail.com

#Generating a new SSH key and adding it to the ssh-agent

#Generating a new SSH key
ssh-keygen -t ed25519 -C "FesalProgramming@gmail.com"
enter
te dice que created directory "/C/User/Fesal/.ssh"

luego pide que entres el passphrase, esto lo dejas vacio y le das enter
vuelve a preguntar confirmacion y das enter nuevamente.
Sale un texto para informar que las claves ssh se han generado exitosamente
# Primero nos movemos a la carpeta .ssh de la siguiente manera:
cd ~/.ssh

# Ya dentro de la carpeta .ssh con la siguiente linea de codigo puedes ver una lista de los archivos que hay dentro de ella.

ls -lrta

#Para ver la key privada en gitbash escribe la sig linea:
cat id_ed25519

Para la llave publica
cat id_ed25519.pub

Luego ir al explorador (carpeta donde se instalo el .ssh)
C:\Users\fesal\.ssh
Encontraras 2 archivos, el de abajo es el publico. lo seleccionas y lo abres con VSC y copias la key y la pegas en un editor como block de notas.

Key ssh publico:
ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIJfN1aVbU5ZEdIOkshzN3wnN2Tnxk8NedHnf+1tjlLQu FesalProgramming@gmail.com

#Agregar la Public Key a la cuenta de GitHub
abrir GitHub y hacer click en la foto de perfil de la izquierda, seleccionar setting y luego hacer click en SSH and GPG KEYS
Hacer click en New SSH key, dar un nombre descrip tivo y pegar la key publica en el espacio reservado para la key y click en Add ssh key y listo eso es todo por el lado de github.

Siguiente paso:
$ADDING SSH KEY AL SSH-AGENT
primero
# start the ssh-agent in the background.
#copiar y pegar esta linea de comando en gitbash
eval "$(ssh-agent -s)" #esta linea inicia (start) el agente

segundo
#add your SSH private key to the ssh-agent. copiar y pegar esta linea de comando en gitbash y enter y enter en las passphrase.
ssh-add c:/Users/fesal/.ssh/id_ed25519

y enter y enter en las passphrase. Listo la clave privada queda agregada al agente.
El agente se encarga de verificar que la clave publica instalada en github y la clave privada instalada localmente en nuestra pc hagan match para permitir transacciones como: clonar, push, pull en proyectos colaborativos.

Esto es todo, ya se puede clonar repositorios o subir repositorios

# Para clonar, desde gitbash, localmente un repositorio que se encuentra en github (puede ser publico o privado):
. Escribir cd Desktop/
# luego copiar el ssh del repositorio a clonar:
. git clone git@github.com:FesalProgrammer/i_can_win.git
enter y listo.
. Buscar la carpeta en el escritorio en la barra inferior (Desktop file explorer) y abrir con VSC.
. Abrir i_can_win usando VSC.
. Crear un archivo (por ejemplo un .txt)
. git add .
. git commit -m "primer commit"
. git push -u origin main 
Se debe verificar que el repositorio en gitub se haya actualizado con el archivo .txt
listo.

Describe all the steps to make possible the following task: This task is performed immediately after the previous one (I Can Win).

1. Add a .gitignore file to the project and configure it to hide files with the extension .db, .log and directories with the names target or bin.

2. Create a feature branch and add two commits to it

3. Merge the feature branch in master

4. Return to feature and create the arrows.txt file with the following contents:

The ship glides gently on the waves
As day turns into night

Make a commit.

5. Go to master. Create the arrows.txt file there and add the following text:

One thousand burning arrows

Fill the starlit sky

Make a commit.

6. Merge feature in master resolving the conflict: save all 4 lines in arrows.txt file in the order they were added in steps 4 and 5.

Here are the detailed steps to accomplish your task:

Add a .gitignore file:

Create a file named .gitignore in your project root.
Add these lines:

*.db
*.log
target/
bin/

Here are the detailed steps to accomplish your task:

1. Add a .gitignore file:
   - Create a file named .gitignore in your project root.
   - Add these lines:
     ```
     *.db
     *.log
     target/
     bin/
     ```

2. Create a feature branch and add two commits:
   - Initialize git (if not already): git init
   - Add and commit .gitignore: git add .gitignore && git commit -m "Add .gitignore"
   - Create and switch to a feature branch:
     git checkout -b feature
   - Make your first change (e.g., touch a file or edit song.txt), git add, and git commit -m "First feature commit"
   - Make a second change, git add, and git commit -m "Second feature commit"

3. Merge the feature branch into master:
   - Switch to master:
     git checkout master
   - Merge feature: git merge feature

4. Return to feature and create arrows.txt:
   - Switch to feature: git checkout feature
   - Create arrows.txt with:
     ```
     The ship glides gently on the waves
     As day turns into night
     ```
   - git add arrows.txt
   - git commit -m "Add arrows.txt with ship poem"

5. Go to master and create arrows.txt with different content:
   - Switch to master:
     git checkout master

   - Create arrows.txt with:
     ```
     One thousand burning arrows

     Fill the starlit sky
     ```
   - git add arrows.txt 
   - git commit -m "Add arrows.txt with arrows poem"

6. Merge feature into master, resolve conflict:
   - git merge feature
   - When the conflict in arrows.txt appears, edit arrows.txt in git editor (select combine incoming + current) so it contains all 4 lines in this order.
   - Edita el conflicto en el editor git que el programa sugiere. de entre las dos opciones selecciona "accept Combine incoming + current", y despues resolver en el editor. en la parte baja el editor se muestran las lineas propuestas, edita manualamente, separando el segundo parrafo del primero con un enter y cuando quede como quieres lo cierras.
   Asi debe quedar reuelto el conflicto:
     ```
     The ship glides gently on the waves
     As day turns into night
     One thousand burning arrows
     Fill the starlit sky
     ```
 y continuas con los siguientes pasos:
- git add arrows.txt
- git commit -m "Merge feature into master, resolve arrows.txt conflict with all lines"
- git push
   
Then:
- git add arrows.txt
- git commit -m "Merge feature into master, resolve arrows.txt conflict with all lines"

how to solve the following error: error: pathspec 'master' did not match any file(s) known to. 

This error means the master branch does not exist in your repository. To solve it:

1. Check your current branches:  
   git branch

2. If you see main but not master, your default branch is named main.  
   To create master from your current branch:  
   git checkout -b master

Or, if you want to rename main to master:  
git branch -m main master

After this, you can switch to master with git checkout master.


