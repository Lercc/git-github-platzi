# Git - Platzi

<div align="center">
  <img src="./md/git.png" alt="git logo" height="300px">
  <h5 style="font-weight:bold;" >Git & GitHub by aomine</h5>
</div>

## Index

- [Introducción](#introducción)
  - [¿Qué es Git?](#qué-es-git)
  - [¿Porqué usar Git?](#porqué-usar-git)
  - [Instalar Git en Windows](#instalar-git-en-windows)
  - [Archivos binarios y de texto plano](#archivos-binarios-y-de-texto-plano)
  - [Terminal y linea de comandos](#terminal-y-linea-de-comandos)
- [Comandos básicos de git](#comandos-básicos-de-git)
  - [Notas](#notas)
  - [git init](#git-init)
  - [git add](#git-add)
  - [git status](#git-status)
  - [git commit](#git-commit)
  - [git log](#git-log)
  - [git checkout](#git-checkout)
  - [git branch](#git-branch)
  - [Ramas](#ramas)
  - [merge](#merge)
  - [git config](#git-config)
  - [git show](#git-show)
  - [git diff](#git-diff)
  - [git reset](#git-reset)
  - [git rm](#git-rm)
- [Flujo de trabajo básico](#Flujo-de-trabajo-básico)
  - [git clone](#git-clone)
  - [git push](#git-push)
  - [git fetch](#git-fetch)
  - [git merge](#git-merge)
  - [git pull](#git-pull)
- [Trabajando con repositorios remotos](#Trabajando-con-repositorios-remotos)
  - [git remote](#git-remote)
  - [SSH](#SSH)
  - [alias](#alias)
  - [git tag](#git-tag)
  - [gitk](#gitk)

## Introducción

### ¿Qué es Git?

Es un control de versiones que guarda los cambios de archivos.

<div align="center">
  <img src="./md/git-1.jpg" alt="img">
</div>

Ademas manejas los cambios que otras personas hagan sobre los mismos archivos, así multiples personas pueden trabajar en un mismo proyecto sin pisarse.

<div align="center">
  <img src="./md/git-2.jpg" alt="img">
</div>

Si existe algun error se peude saber quien hizo ese cambio.

<div align="center">
  <img src="./md/git-3.jpg" alt="img">
</div>

si hay algo de una versión antigua que quieres recuperar  lo puedes hacer de manera precisa.

<div align="center">
  <img src="./md/git-4.jpg" alt="img">
</div>

En tu maquina local usas git funciona en la terminal o linea de comandos.

<div align="center">
  <img src="./md/git-5.jpg" alt="img">
</div>

Y tiene distintos comandos.

<div align="center">
  <img src="./md/git-6.jpg" alt="img">
</div>

#### Si quieres
* Colaborar con otros
* Usar una interfaz web
* Publicar tus proyectos en la web

Usas GitHub

<div align="center">
  <img src="./md/git-7.jpg" alt="img">
</div>

<div align="right">
  <small><a href="#index">🡡 volver al inicio</a></small>
</div>

### ¿Porqué usar Git?
Usamos Git solo para cambiar los cambios realizados en un archivo.

* Donde ocurrieron
* Cuando ocurrieron
* Quien los hizo
* Poder vovler a ellos

Git fue creado por la fundación Linux principalmente por Linus Torbal y es el sistema que maneja el kernel de linux.

<div align="right">
  <small><a href="#index">🡡 volver al inicio</a></small>
</div>

### Instalar Git en Windows

Asegurate de instalar git bash here 

<div align="center">
  <img src="./md/git-8.jpg" alt="img">
</div>

Para una fuente suave en la linea de comandos

<div align="center">
  <img src="./md/git-9.jpg" alt="img">
</div>

Cambiar el editor visual por defecto de git

<div align="center">
  <img src="./md/git-10.jpg" alt="img">
</div>

Estas opciones tienen que ver con que windows no es un entorno amigable para programadores.

Git se encarga de instala git bsah para hacernos la vida más facil (sololo podremos usar git en git bash)

<div align="center">
  <img src="./md/git-12.jpg" alt="img">
</div>

Pero tambien podemos usar git desde la linea de comandos nativa de windows y de terceros (git bash)

<div align="center">
  <img src="./md/git-11.jpg" alt="img">
</div>

EL tipo de libreria que queremos usar para la seguridad

OpenSSL es una libreria nativa de Linux y Unix para que toda tu información este cifrada y protegida pero esta no esta instalada por defecto en windows

Pero windows tiene sus propias librerias con la que manejas la seguridad a nivel de microsoft.

<div align="center">
  <img src="./md/git-13.jpg" alt="img">
</div>

Windows y Linux manejan el enter de forma distinta, ahora se nos presentan 3 opciones

* nos encargamos nosotros
  * se reciben los enter al estilode windows y cuando se envian al repositorio se convierten a la manera de linux
* te encargas tú
  * Como este en el sistema operativo
* se lo dejamos a una fuerza superior xd
  * no se realizan conversiones

La primera version te hace más comptible con todo el mundo :)

<div align="center">
  <img src="./md/git-14.jpg" alt="img">
</div>

Ahora te pregunta si quieres usar su emluador de linux (MinTTY) o la consola por defecto de windows

<div align="center">
  <img src="./md/git-15.jpg" alt="img">
</div>

3 opciones más
* File system caching
  * Guardar todo en un cache del sistema
* Git Credentials Manager
  * Una forma en la que se manejan y se guardan las llaves privadas de git pero en el entorno de windows 
* Symbolic Links
  * Es como los accesos directos de windows pero que funciona en linux

<div align="center">
  <img src="./md/git-16.jpg" alt="img">
</div>

<div align="right">
  <small><a href="#tabla-de-contenido">🡡 volver al inicio</a></small>
</div>

### Archivos binarios y de texto plano

Los archivos de texto plano se muestran tal cual como se ven y puede ser abierto por editores de textos mientras que los archivos binarios estan estructuradas en ceros y unos en este caso word lo entiende y lo muestra graficamente mientras que uneditor de texto no lo entiende.

En el mundo de got lo que nosotros vamos a poder editar es texto plano.

<div align="right">
  <small><a href="#index">🡡 volver al inicio</a></small>
</div>

### Terminal y linea de comandos

Lo primero que hay que entender es la diferencia de estructura de archivos entre windows y linux

* pwd
  * Muestra la ruta actual
* cd (change directory)
  * Movernos entre los directorios
  * si se nos muestra un ~ -> nos encontramos en user
  * si se nos muestra un / -> nos encontramos en la raiz del disco
  * cd ../ para salir del directorio 
  * cd / -> para ir a la raiz de mi disco
  * cd -> para ir a mi usuario 
  * echo cd RUTA >> ~.bashrc
* ls
  * mostros todos los archivos del directorio
  * ls -l -> mostrar todos los archivos y que me los muestre en una lista
  * ls -a -> mostrar todos los archivos incluidos los ocultos
  * ls -al -> mostrar todos los archivos incluidos los ocultos y que me los muestre en una lista
* clear
  * limpiar la consola
  * tambien podemos usar ctrl + l
* Windos no es sensible a mayusculas puedes ingrear a User com cd User o cd user (esto no es así en mac o linux)
* tab
  * te autocompleta la sentencia cd u + tab -> cd Users/
* mkdir (make directory)
  * para crear una carpeta
* touch
  * para crear un archivo
* cat
  * para ver el contenido de un archibo de texto plano
* history
  * para ver el historial de comandos
* !NUMERO_DEL_COMANDO
  * para ejecutar ese comando
* rm (remove)
  * remover archivos
  * rm -r -> para borrar directorios 
* COMANDO --help
  * ver la lista de parametros para cada comando

<div align="right">
  <small><a href="#index">🡡 volver al inicio</a></small>
</div>

## Comandos básicos de git

### Notas

#### -

Se usa un solo guión cuando vas a usar solo las letras (atajos) -m

#### --

Usar el doble guion significa que vas a usar una palabra como --global

#### <ESC> + :wq

Para salir de lugares raros :v

<div align="right">
  <small><a href="#index">🡡 volver al inicio</a></small>
</div>

### git init

Suceden 2 cosas

* Se crea un area en memoria ram que se llama staging donde se iran agregando los cambios.
* Se crea el repositorio ( la carpeta .git) y es donde  van a estar todos los cambios al final de tu proyecto.

<div align="right">
  <small><a href="#index">🡡 volver al inicio</a></small>
</div>

### git add

#### git add <FILE_NAME> or .

Una vez haces cambios en tus archivos se agregan al staging area usando el comando git add . todos los archivos modificados pasan a vivir en staging donde esperan a que se envie al repositorio.

Antes de ejecutar el comando los archivos no son rastreados (untracked) y no estan el staging y una vez se ejecute el comando estos pasan a ser rastreados (tracked) y pasan a estar en staging

<div align="right">
  <small><a href="#index">🡡 volver al inicio</a></small>
</div>

### git status

Para saber que archivos estan el staging

<div align="right">
  <small><a href="#index">🡡 volver al inicio</a></small>
</div>

### git commit

Todos los archivos modificados y que vivian en staging pasan al repositorio por defecto llamado master.

Los números raros que salen en cada commit son el id en la base de datos.

Cada commit enviado al repositorio es una nueva version de cambios de tu proyecto v1, v2, v3... vn.

Al usarlo se nos abrira una pantalla rara que es un editor de codigo dentreo del mundo de git llamado vim

#### git commit -m "MENSAJE"

Para poder agregarle un mensaje a tu commit (es lo más recomendable)

#### git commit -a

esto atuomaticamente hace el git add de los cambios __Solo funciona con archivos que ya estabam el staging previamente__ si creo un archivo nuevo esto no va a funcionar.

#### git commit -am "MENSAJE"

juntamos los 2 comandos anteriores

<div align="right">
  <small><a href="#index">🡡 volver al inicio</a></small>
</div>

### git log

Para ver todo el historial de commits

#### git log --stat

vamos a poder ver los cambios especificos de los archivos en cada cmommit 

#### git log --all

Te muestra todo el historial de tus commits

#### git log --all -graph

Te muestra todo el historial de tus commits con un gráfico

#### git log --all -graph --decorate --oneline

Te muestra todo el historial de tus commits con un gráfico y comprimido

#### :q

Para salir del log

<div align="right">
  <small><a href="#index">🡡 volver al inicio</a></small>
</div>

### git checkout

#### git checkout -- <FILE_NAME>

Para eliminar los cambios que no se han subido la staging

#### git checkout <COMMIT_ID>

Puedes traer las distinas versiones (commits) hacia tu carpeta.

#### git checkout <COMMIT_ID> <FILE_NAME>

Puedes traer las distinas versiones (commits) hacia tu carpeta pero solo de el archivo especifico.

#### git checkout <BRANCH_NAME>

Te permite moverte entre distintas ramas.

#### git checkout -b <BRANCH_NAME>

Te ptermite crear y moverte a la rama nueva.

<div align="right">
  <small><a href="#index">🡡 volver al inicio</a></small>
</div>

### git branch

Te muestra las ramas existentes

#### git branch <NAME>

Te permite crear una rama

#### git branch -d <NAME>

Te perimte eliminar una rama, pero solo si esta no contiene trabajos sin fucionar

Si se esta trabajando con un repositorio remoto entonces se tiene que hacer un push

```
git push -u origin :<BRANCH_NAME>
```

#### git branch -D <NAME>

te permite forzar la eliminacion de la rama

Si se esta trabajando con un repositorio remoto entonces se tiene que hacer un push

```
git push -u origin :<BRANCH_NAME>
```

<div align="right">
  <small><a href="#index">🡡 volver al inicio</a></small>
</div>

### Ramas

Por defecto tu estas en una rama master con sus distintas versines (commits)

```
Master      v1   ->   v2   ->   v3   ->   v-actual
```

Pero ahora decidimos hacer algunos experimentos pero no queremos tocar el código actual asi que creamos una rama llamada Development teniendo como base la v3 del proyecto.

Master      v1   ->   v2   ->   v3   ->   v-actual

↓ (v3 of Mater to v1 of Development)

Development                     v1(v3)   ->  v2   ->   v3

La rama Development se convirtio en algo completamente distinto a la de master

Ahora digamos que estabas cambiando cosas y salio un bug en la versión actual por lo cual creas una rama especial partiendo de la versión actual de la rama master.

Master      v-actual

↓ (v-actual of Mater to v1 of HotFix)


HotFix         v1(v-actual)         ->       v2

Ahora que ya solucionaste el bug en otra rama es momento de llevar esos cambios a la version actual en la rama master

<div align="right">
  <small><a href="#index">🡡 volver al inicio</a></small>
</div>


### merge

Ahora que ya tienes la versin de HotFix en Master se creo una nueva version que llamaremos version final

Master      v-actual         v-final

↓ (v-actual of Master to v1 of HotFix) - ↑ (v2 of HotFix to Master in v-final)

HotFix         v1         ->       v2

Pero ahora ya terminaste tus experimentos y quieres unirlos a la version final en la rama master

Master                 v-final   ->   v-final-final

↑ (v3 of Development to Master in v-final-final)

Development          v3

Pero juntar 2 ramas puede romper con el código y a esto se le llama conflicto.

<div align="right">
  <small><a href="#index">🡡 volver al inicio</a></small>
</div>

### git config

Te mostrara una lista de como usarlo

#### git config --lsit (-list)

Te mostrara la configuración de tu git

#### git config --list --show-origin

Podras ver donde estan guardadas las configuraciones de windows

#### git config --global

Para cambiar la configuración global de git

##### git config --global user.name "<NAME>"

Para cambiar el usuario de la configuración global

##### git config --global user.email "<EMAIL>"

Para cambiar el email de la configuración global

#### git config --global ailas.<ALIAS> "<COMAND WITHOUT GIT>"

crear alias para un comando de git

<div align="right">
  <small><a href="#index">🡡 volver al inicio</a></small>
</div>

### git show

Te muestra todos los cambios de tu proyecto entre el commit actual y el anterior

#### git show <FILE_NAME>

Te muestra todos los cambios de un archivo entre el commit actual y el anterior

#### git show-ref --tags

Te muestra los tags con su hash

#### git show-branch

Te muestra la historia de tus ramas

#### git show-branch --all

Te muestra la historia de tus ramas pero con más detalles

<div align="right">
  <small><a href="#index">🡡 volver al inicio</a></small>
</div>

### git diff

Te muestra los cambios entre tus archivos locales y lo que este en staging (los que estan siendo rastreados, que se les hizo como minimo 1 git add)

#### git diff <COMMIT_ID> <COMMIT_ID>

Te muestra todos los cambios entre los distintos commit

<div align="right">
  <small><a href="#index">🡡 volver al inicio</a></small>
</div>

### git reset 

#### git reset --hard

Para volver en el tiempo borrando absolutamente todo lo que este por adelante del punto al cual deseamos volver

#### git reset --soft

Similiar a --hard pero mantenemos lo que este en staging

#### git reset HEAD <FILE_NAME>

Elimina todos los archivos que se esten rastreando en el staging

<div align="right">
  <small><a href="#index">🡡 volver al inicio</a></small>
</div>

### git rm

No se puede usar sin más tiene que tener un flag

#### git rm --cached <FILE_NAME>

Elimina los archivos del área de Staging y del próximo commit pero los mantiene en nuestro disco duro.

Funciona similiar a git reset HEAD

#### git rm --force <FILE_NAME>

Elimina los archivos de Git y del disco duro. Git siempre guarda todo, por lo que podemos acceder al registro de la existencia de los archivos, de modo que podremos recuperarlos si es necesario (pero debemos usar comandos más avanzados).

<div align="right">
  <small><a href="#index">🡡 volver al inicio</a></small>
</div>

## Flujo de trabajo básico

Antes que nada se necesita un repositorio remoto puede ser github, gitlab, bitbucket el que quieras

### git clone

#### git clone <REPOSITORY_URL>

Se trae lor archivos a dos lugares, una copia del master a tu directorio local y crea la base de datos de todos los cambios historicos en el repositorio local y deja staging limpio.

<div align="center">
  <img src="./md/git-17.jpg" alt="img">
</div>


<div align="right">
  <small><a href="#index">🡡 volver al inicio</a></small>
</div>

### git push

Envio todos mis commits de mi repositorio local al servdior remoto

<div align="center">
  <img src="./md/git-18.jpg" alt="img">
</div>


#### git push <REMOTE | origin por lo general> <BRANCH_NAME | master por lo general>

Comando pra enviar al repositorio remoto los commits de mi rama especifica

#### git push <REMOTE | origin por lo general> --tags

Para enviar los tags

#### git push <REMOTE | origin por lo general> :refs/tags/<TAG_NAME>

Para eliminar un tag en el repositorio remoto

<div align="right">
  <small><a href="#index">🡡 volver al inicio</a></small>
</div>

### git fetch

Te trae los nuevos commits del repositorio remoto al repositorio local pero NO los trae a nuestro directorio de trabajo local

<div align="center">
  <img src="./md/git-19.jpg" alt="img">
</div>


<div align="right">
  <small><a href="#index">🡡 volver al inicio</a></small>
</div>

### git merge

Para que se copie en nuestro directorio de trabajo local tengo que fucionar los ultima version que esta en el repositorio local con mi version actual (la de mi directorio de trabajo local)

<div align="center">
  <img src="./md/git-20.jpg" alt="img">
</div>

#### git merge <BRANCH_NAME>

Te permite unir 2 ramas

<div align="right">
  <small><a href="#index">🡡 volver al inicio</a></small>
</div>

### git pull

Ejecuta fetch y merger a la vez para traer los ultimos cambios en el repositorio remoto y combinarlos con nuestro repositorio global y directorio global en un solo paso

<div align="center">
  <img src="./md/git-21.jpg" alt="img">
</div>


#### git pull <REMOTE | origin por lo general> <BRANCH_NAME | master por lo general>

Para poder subitr los commits al repositorio remoto

#### git pull <REMOTE | origin por lo general> <BRANCH_NAME | master por lo general> --allow-unrelated-histories

Para poder subitr los commits al repositorio remoto de manera forzada

<div align="right">
  <small><a href="#index">🡡 volver al inicio</a></small>
</div>

## Trabajando con repositorios remotos

### git remote 

Nos muestra los remotes existentes

#### git remote add origin <NEW_URL>

Para poder agregar la url del repositorio remoto de donde nos traeremos los cambios y hacia donde enviaremos nuestros cambios

#### git remote -v

Nos muestra vervalmente los remotes existentes

#### git remote rm <REMOTE_NAME>

Nos permite eliminar un remote

#### git remote set-url <REMOTE_NAME> <NEW_URL>

Nos permite cambiar la url remota

<div align="right">
  <small><a href="#index">🡡 volver al inicio</a></small>
</div>

### SSH

#### ssh-keygen -t rsa -b 4096 -C "<MESSAGE>"

Generar llave publica y privada

#### eval $(ssh-agent -s)

Comprobar si el sistema de cifrado está activo

#### ssh-add <SECRET_KEY_ROUTE>

Informar al sistema la ubicación de nuestra llave privada

<div align="right">
  <small><a href="#index">🡡 volver al inicio</a></small>
</div>

### alias

te muestra los alias creados

#### alias <ALIAS_NAME>=<"COMAND">

crear un alias para un comando

<div align="right">
  <small><a href="#index">🡡 volver al inicio</a></small>
</div>

### git tag

Te muestra los tags

#### git tag -a <TAG_NAME> -m "<MESSAGE>" <COMMIT_ID>

Agregar un tag

#### git tag -d <TAG_NAME>

Eliminarar un tag

<div align="right">
  <small><a href="#index">🡡 volver al inicio</a></small>
</div>

### gitk

nos abre un gestor visual de las historias de git

<div align="right">
  <small><a href="#index">🡡 volver al inicio</a></small>
</div>