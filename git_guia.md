-----PUBLIC KEY-----
ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIDpPaisA1QNkS1IV2fTYjRW4tQgdjr1C6pte6KKzRHxz fesalprogramming@gmail.com

# Como hago para ver si tengo instalado git
Para verificar si tienes Git instalado en Windows, puedes hacerlo fácilmente desde la consola.

Paso 1. Abrir la terminal
Puedes utilizar cualquiera de estas opciones:

Presiona las teclas Windows + R.

Escribe cmd.

Presiona Enter.

También puedes abrir PowerShell o la terminal de Visual Studio Code.

Paso 2. Ejecutar el comando
Escribe el siguiente comando:

git --version

Presiona Enter.

Paso 3. Interpretar el resultado
Git instalado
Si aparece algo parecido a esto:

git version 2.45.1.windows.1

¡Perfecto! Git está instalado en tu computadora.

Git no instalado o no reconocido
Si aparece este mensaje:

'git' no se reconoce como un comando interno o externo

Significa que Git no está instalado o que no está configurado en el PATH de Windows.

Paso 4. Si no tienes Git
Puedes descargarlo desde su página oficial:

Descargar Git para Windows.

Cuando ejecutes git --version, dime qué resultado te aparece y te ayudo con el siguiente paso.

También podemos continuar con la configuración de Git en Visual Studio Code.  Configurar Git en VS Code

Ayúdame a configurar Git en Visual Studio Code paso a paso en Windows.
¡Perfecto! Vamos a configurar Git en Visual Studio Code (VS Code) en Windows, paso a paso y desde cero.

El objetivo es que puedas utilizar Git para guardar versiones de tus proyectos, registrar cambios y subir tu código a GitHub.

Paso 1. Verificar que Git esté instalado
Abre Visual Studio Code.

En el menú superior, selecciona Terminal → New Terminal (Nueva terminal).

Escribe:

git --version

Si aparece algo parecido a:

git version 2.45.1.windows.1

Git instalado correctamente
Si no reconoce el comando, primero debes instalar Git desde su página oficial:

Descargar Git para Windows.

Paso 2. Configurar tu nombre y correo electrónico
Git necesita saber quién realiza los cambios en los proyectos.

En la terminal de VS Code ejecuta:

git config --global user.name "Fesalprogrammer"

Luego:

git config --global user.email "Fesalprogramming@gmail.com"

Utiliza el correo que quieras asociar a tus proyectos de GitHub.

Para comprobar la configuración:

git config --global --list

Deberías ver:

user.name= Fesalprogrammer
user.email= Fesalprogramming@gmail.com
credential.https://autocode.git.epam.com.provider=generic

Paso 3. Comprobar que VS Code reconoce Git
Observa la barra lateral izquierda de VS Code.

Busca el icono de Control de código fuente (Source Control).

Haz clic sobre él.

How to easily delete Git Branches in Visual Studio Code | bobbyhadz
Si Git está correctamente instalado, VS Code debería reconocerlo automáticamente.

Paso 4. Crear tu primer repositorio Git
Vamos a practicar con un proyecto sencillo.

1. En tu computadora, crea una carpeta llamada:

C:\Proyectos\git-practice
En VS Code, selecciona File → Open Folder.

Busca y abre la carpeta git-practice.

Presiona Ctrl + Shift + G para abrir Control de código fuente.

Selecciona Initialize Repository (Inicializar repositorio).

How To Use Git Integration in Visual Studio Code | DigitalOcean
¡Ya tienes tu primer repositorio Git local!

Esto significa que Git comenzará a controlar los cambios que realices dentro de esa carpeta. Todavía no has subido nada a Internet. 

Paso 5. Crear tu primer archivo
En el explorador de archivos de VS Code, crea un archivo llamado README.md.

Escribe lo siguiente:

# Mi primer proyecto con Git

Estoy aprendiendo a utilizar Git y GitHub.
Guarda el archivo con Ctrl + S.

Regresa a Control de código fuente.

Verás que aparece README.md en la sección Changes.

La letra U significa que es un archivo nuevo que Git todavía no está siguiendo.

Paso 6. Guardar tu primer cambio (Commit)
Este es uno de los pasos más importantes.

3 Ways to Backup Your Code (Even If You Don’t Know Git) - En la sección Changes, pulsa el signo + que aparece junto a README.md.

El archivo pasará a Staged Changes.

En el campo de mensaje escribe:

Mi primer commit
4. Pulsa el botón Commit.

¡Primer commit realizado!
Acabas de guardar una versión de tu proyecto en el historial local de Git.

Importante: Commit guarda los cambios localmente, pero no los sube a GitHub. 

Paso 7. Conectar VS Code con GitHub (opcional)
Git y GitHub son herramientas diferentes:

Git: controla las versiones de tu código en tu computadora.

GitHub: permite almacenar tus repositorios en Internet y compartirlos.

Bridging the Gap: Understanding Git, GitHub, and Engineering Collaboration for Non-Tech PMs
Para conectarlos:

Crea una cuenta en GitHub.

En VS Code presiona Ctrl + Shift + P.

Escribe Publish to GitHub.

Selecciona esa opción.

VS Code te solicitará iniciar sesión en GitHub.

Sigue las instrucciones del navegador.

Elige el nombre del repositorio.

Selecciona Private para que sea privado durante esta práctica.

Confirma la publicación.

¡Listo! Tu proyecto estará publicado en GitHub. 

Paso 8. Los cinco comandos Git que debes conocer
Comando

Función

git status

Ver el estado de los archivos

git add .

Preparar todos los cambios

git commit -m "mensaje"

Guardar una versión

git push

Subir cambios a GitHub

git pull

Descargar cambios de GitHub

Comprobemos cómo vas
Quiero que avancemos de manera práctica, sin saltarnos pasos.

1. ¿Pudiste ejecutar git --version?


Sí, aparece la versión de Git.

Configuré nombre y correo.

Inicialicé el repositorio.

Realicé mi primer commit.

Publiqué el proyecto en GitHub.
Mi propuesta es que aprendamos Git y GitHub trabajando sobre un proyecto real de Java o desarrollo web. Así podrás practicar lo que se utiliza en un equipo de desarrollo profesional.

Mi situación con Git en Windows y VS Code: git --version: yes. Cuenta de GitHub: yes. Mi avance: 0. Continúa guiándome paso a paso.
¡Excelente! Ya tenemos dos cosas importantes: Git está instalado y tienes una cuenta de GitHub. Ahora vamos a comenzar desde cero y avanzar juntos, paso a paso.

Vamos a utilizar Visual Studio Code y Windows.

Etapa 1. Configurar Git en VS Code
Git instalado Cuenta GitHub disponible

Paso 1. Abrir Visual Studio Code
Abre Visual Studio Code.

En el menú superior, selecciona Terminal.

Haz clic en New Terminal (Nueva terminal).

Deberías ver una ventana de terminal en la parte inferior.

Paso 2. Configurar tu identidad
Vamos a indicarle a Git quién eres.

Primero escribe este comando:

git config --global user.name "Tu Nombre"

Reemplaza Tu Nombre por el nombre que quieres que aparezca en tus contribuciones.

Ahora escribe:

git config --global user.email "tu_correo@gmail.com"

Utiliza el correo asociado a tu cuenta de GitHub, preferentemente.

Paso 3. Verificar la configuración
Escribe:

git config --global --list

Deberías obtener algo parecido a:

user.name=Tu Nombre
user.email=tu_correo@gmail.com
Si aparecen ambos datos, la configuración está correcta.

Tu primera tarea
Antes de continuar, quiero que realices estos pasos y comprobemos que todo funciona.

Lista de comprobación

Abrí la terminal de VS Code.

Configuré mi nombre y correo electrónico.

Ejecuté git config --global --list.

Importante: No compartas contraseñas ni tokens de GitHub.

Cuando terminemos esta etapa, crearemos nuestro primer repositorio, guardaremos un archivo con commit y finalmente lo publicaremos en GitHub.

Vamos a hacerlo como una práctica real de desarrollo de software.

Ya completé la configuración inicial de Git en VS Code. Quiero continuar con la creación de mi primer repositorio local.
¡Excelente! Ya configuramos Git. Ahora vamos a crear tu primer repositorio local, utilizando Visual Studio Code en Windows.

Un repositorio es una carpeta de proyecto que Git controla para registrar los cambios que vas realizando en tus archivos.

Etapa 2. Crear tu primer repositorio local
Paso 1. Crear una carpeta para el proyecto
En Windows:

Abre el Explorador de archivos.

Ingresa en el disco C:.

Crea una carpeta llamada Proyectos.

Dentro de ella crea otra carpeta llamada mi-primer-repositorio.

La estructura debe quedar así:

C:/Proyectos/mi-primer-repositorio

Paso 2. Abrir la carpeta en VS Code
Abre Visual Studio Code.

Selecciona File → Open Folder.

Busca C:\Proyectos\mi-primer-repositorio.

Haz clic en Seleccionar carpeta.

Ahora VS Code tiene abierto tu proyecto.

Paso 3. Inicializar el repositorio Git
Abre la terminal de VS Code:

Menú Terminal → New Terminal.

Escribe el siguiente comando:

git init

Presiona Enter.

Deberías ver un mensaje parecido a:

Initialized empty Git repository in
C:/Proyectos/mi-primer-repositorio/.git/
Repositorio creado
¿Qué acaba de suceder?

Git creó una carpeta oculta llamada .git dentro de tu proyecto.

Esta carpeta contiene la información necesaria para administrar las versiones de tus archivos.

Importante: No debes borrar ni modificar manualmente esa carpeta.

Paso 4. Verificar el repositorio
En la misma terminal escribe:

git status

Deberías obtener algo parecido a:

On branch master

No commits yet

nothing to commit
Dependiendo de tu configuración, puede aparecer main en lugar de master. Ambos resultados son posibles.

Esto significa que Git ya está funcionando dentro de tu proyecto.

Paso 5. Crear tu primer archivo
Ahora vamos a crear un archivo para nuestro proyecto.

En el panel Explorer de VS Code, haz clic en el icono de nuevo archivo.

Escribe el nombre:

README.md

3. Dentro del archivo escribe:

# Mi primer repositorio Git

Este es mi primer proyecto utilizando Git
y Visual Studio Code.

Estoy aprendiendo a controlar versiones.
4. Guarda el archivo presionando Ctrl + S.

Add a README file to your GitHub repo 📖
Paso 6. Verificar los cambios
Regresa a la terminal y ejecuta:

git status

Ahora deberías observar algo similar a:

Untracked files:

    README.md
¿Qué significa Untracked?

Significa que Git detectó el archivo, pero todavía no lo está siguiendo para registrar sus cambios.

¡Esto es exactamente lo que queremos!

Comprobemos tu avance
¿Pudiste completar estos pasos?

1. ¿Ejecutaste git init?
   Sí, se creó el repositorio.
   No, apareció un error.
2. ¿Creaste el archivo README.md?
   Sí, ya está creado.
   Todavía no.
3. ¿Qué resultado obtuviste al ejecutar git status?
   Aparece README.md como Untracked.
   Aparece otro resultado o un error.
   ¿Qué haremos después?

En la siguiente etapa aprenderemos tres conceptos fundamentales:

git add: preparar los archivos.

git commit: guardar una versión del proyecto.

git log: consultar el historial de versiones.

Estos tres conceptos son fundamentales para trabajar profesionalmente con Git.


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


Para abrir la terminal gitbash:
1. click simbolo window en la barra inferior y escribir git, hacer click en gitbash
2. Tambien se puede hacer en la terminal de VS code al lado del simbolo + hacer click y seleccionar gitbash de la lista desplegada.

Checking for existing SSH keys
Before you generate an SSH key, you can check to see if you have any existing SSH keys.

Open Git Bash.
Para abrir gitbash:
1. click simbolo window y escribir git, hacer click en gitbash
2. Tambien se puede abrir VSC y abrir una NEW TERMINAL y  al lado del simbolo + (en la terminal) hacer click y seleccionar gitbash de la lista desplegada(si es que esta instalado, sino habria que instalar GIT).

texto ejemplo de la terminal gitbash:
Fesal@DESKTOP-EACSNF6 MINGW64 ~
$
verificar que el path termina exactamente en el nombre de usuario.

Enter ls -al ~/.ssh to see if existing SSH keys are present.

$ ls -al ~/.ssh #copiar y pegar este codigo en gitbash (no incluir simbolo $)

PARA SALIR (logout) DE GITBASH => EXIT
PARA LIMPIAR DE GITBASH => CLEAR

SI TE ENCUENTRAS EN EL DIRECTORIO INICIAL: Fesal@DESKTOP-EACSNF6 MINGW64 ~

PARA CAMBIAR AL ESCRITORIO => cd Desktop/
Fesal@DESKTOP-EACSNF6 MINGW64~/Desktop

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
ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIDpPaisA1QNkS1IV2fTYjRW4tQgdjr1C6pte6KKzRHxz fesalprogramming@gmail.com

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


