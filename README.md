# Git - Platzi

## Introducción

### ¿Qué es Git?
Es un control de versiones que guarda los cambios de archivos.

![git](./md/git-1.jpg)

Ademas manejas los cambios que otras personas hagan sobre los mismos archivos, así multiples personas pueden trabajar en un mismo proyecto sin pisarse.

![git](./md/git-2.jpg)

Si existe algun error se peude saber quien hizo ese cambio.

![git](./md/git-3.jpg)

si hay algo de una versión antigua que quieres recuperar  lo puedes hacer de manera precisa.

![git](./md/git-4.jpg)

En tu maquina local usas git funciona en la terminal o linea de comandos.
![git](./md/git-5.jpg)

Y tiene distintos comandos.

![git](./md/git-6.jpg)

#### Si quieres
* Colaborar con otros
* Usar una interfaz web
* Publicar tus proyectos en la web

Usas GitHub

![git](./md/git-7.jpg)

###  ¿Porqué usar Git?
Usamos Git solo para cambiar los cambios realizados en un archivo.

* Donde ocurrieron
* Cuando ocurrieron
* Quien los hizo
* Poder vovler a ellos

Git fue creado por la fundación Linux principalmente por Linus Torbal y es el sistema que maneja el kernel de linux.

### Instalar Git en Windows

Asegurate de instalar git bash here 

![git](./md/git-8.jpg)

Para una fuente suave en la linea de comandos

![git](./md/git-9.jpg)

Cambiar el editor visual por defecto de git

![git](./md/git-10.jpg)

Estas opciones tienen que ver con que windows no es un entorno amigable para programadores.

Git se encarga de instala git bsah para hacernos la vida más facil (sololo podremos usar git en git bash)

![git](./md/git-12.jpg)

Pero tambien podemos usar git desde la linea de comandos nativa de windows y de terceros (git bash)

![git](./md/git-11.jpg)

EL tipo de libreria que queremos usar para la seguridad

OpenSSL es una libreria nativa de Linux y Unix para que toda tu información este cifrada y protegida pero esta no esta instalada por defecto en windows

Pero windows tiene sus propias librerias con la que manejas la seguridad a nivel de microsoft.

![git](./md/git-13.jpg)

Windows y Linux manejan el enter de forma distinta, ahora se nos presentan 3 opciones

* nos encargamos nosotros
  * se reciben los enter al estilode windows y cuando se envian al repositorio se convierten a la manera de linux
* te encargas tú
  * Como este en el sistema operativo
* se lo dejamos a una fuerza superior xd
  * no se realizan conversiones

La primera version te hace más comptible con todo el mundo :)

![git](./md/git-14.jpg)

Ahora te pregunta si quieres usar su emluador de linux (MinTTY) o la consola por defecto de windows

![git](./md/git-15.jpg)

3 opciones más
* File system caching
  * Guardar todo en un cache del sistema
* Git Credentials Manager
  * Una forma en la que se manejan y se guardan las llaves privadas de git pero en el entorno de windows 
* Symbolic Links
  * Es como los accesos directos de windows pero que funciona en linux

![git](./md/git-16.jpg)

### Archivos binarios y de texto plano

Los archivos de texto plano se muestran tal cual como se ven y puede ser abierto por editores de textos mientras que los archivos binarios estan estructuradas en ceros y unos en este caso word lo entiende y lo muestra graficamente mientras que uneditor de texto no lo entiende.

En el mundo de got lo que nosotros vamos a poder editar es texto plano.

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
* COMANDO --help
  * ver la lista de parametros para cada comando

## Comandos básicos de git

### git init

Suceden 2 cosas

* Se crea un area en memoria ram que se llama staging donde se iran agregando los cambios.
* Se crea el repositorio ( la carpeta .git) y es donde  van a estar todos los cambios al final de tu proyecto.

### git add

Una vez haces cambios en tus archivos se agregan al staging area usando el comando git add . todos los archivos modificados pasan a vivir en staging donde esperan a que se envie al repositorio.

Antes de ejecutar el comando los archivos no son rastreados (untracked) y no estan el staging y una vez se ejecute el comando estos pasan a ser rastreados (tracked) y pasan a estar en staging

### git commit -m "MENSAJE"

Todos los archivos modificados y que vivian en staging pasan al repositorio por defecto llamado master.

Los números raros que salen en cada commit son el id en la base de datos.

Cada commit enviado al repositorio es una nueva version de cambios de tu proyecto v1, v2, v3... vn.


### git checkout

Puedes traer las distinas versiones (xommita) hacia tu carpeta.

Tambien te permite moverte entre distintas ramas.

### git branch

Te permite crear una rama

#### Ramas

Por defecto tu estas en una rama master con sus distintas versines (commits)

Master      v1   ->   v2   ->   v3   ->   v-actual

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

### git merge

Te permite unir 2 ramas

Ahora que ya tienes la versin de HotFix en Master se creo una nueva version que llamaremos version final

Master      v-actual         v-final

↓ (v-actual of Master to v1 of HotFix) - ↑ (v2 of HotFix to Master in v-final)

HotFix         v1         ->       v2

Pero ahora ya terminaste tus experimentos y quieres unirlos a la version final en la rama master

Master                 v-final   ->   v-final-final

↑ (v3 of Development to Master in v-final-final)

Development          v3

Pero juntar 2 ramas puede romper con el código y a esto se le llama conflicto.