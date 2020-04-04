# Apuntes de git

**git init**
Inicia git en el archivo

**git add .**
Agrega todos los archivos que han sufrido cambios desde el ultimo commit

**git add index.html**
Con *git add archivo* le indicas que archivo agregar.

**git commit -m "Mensaje"**
Confirma los cambios agregados. Es bueno dar un mensaje claro para que asi en el futuro sepas de hiciste.

**git status**
En rojo -> Muestra un pequenho historial de los recientes cambios,
En verde -> muestra que estan agregados pero aun sin confirmar.

**git add *.png**
Agregara solo los archivos con extension .png

**git add css/**
Agregara solo la carpeta css/

**git reset *.xml**
Luego de hacer *git add .* quieres excluir algun archivo puedes dar el nombre del archivo, o como lo indica arriba excluimos todos los archivos con extension .xml

**git add "*.txt"**
Agrega todos los txt de todo el proyecto.

**git add *.txt**
Agrega todos los txt del directorio actual

**git add -all**
Agrega todos los archivos

**git add pdfs/*.pdf**
Agrega todos los .pdf del archivo pdfs

**git log**
Muestra todas las confirmaciones que has hecho.

**git log --oneline**
Resume las confirmaciones en una linea

**git log --oneline --decorate --all --graph**
Muestra los cambios de todas las ramas de modo muy bonito

**git status -s**
Muestra cuales estan  agregados y cuales no
M = modificado

**git status -s -b**
Indica la branch rama en la que estamos trabajando

**git config --global alias.lg "log --oneline --decorate --all --graph"**
Configuramos un alias para asi no estar escribiendo mucho

**git config --global alias.s "status -s -b"**
Otro ejemplo de alias

**git config --global -e**
Muestra las configuraciones globales. Modo de escritura
**git config --global -l**
Muestra las configuraciones globales. Modo de lectura

**git checkout -- .**
vuelve al ultimo commit que se hizo

## Viajes en el tiempo

**git diff**
Historial de los cambios que hicimos. En rojo como estaban antes (en el ultimo commit) y en verde todo lo que cambiamos.

**git diff --staged**
Muestra los cambios de los archivos que estan en el escenario.

**git reset HEAD README.md**

### Deshacer commits y cambiarlos
**git commit --amend -m "Mensaje actualizado"**
Podemos cambiar el mensaje del ultimo commit que hicimos.

**git reset --soft HEAD^**
Este comando va a resetear el ultimo commit y nos permite realizar cambios en el proyecto y luego poder confirmarlos con los anteriores.
HEAD apunta al ultimo commit que hicimos

**git reset --soft id**
Por ejemplo: *git reset --soft 36sf8e6* nos permitira realizar cambios especificamente en ese commit y luego poder confirmarlos en el mismo commit

**git reset --mixed id**
Por ejemplo *git reset --mixed 860s5s2* vuelves a ese commit y los commit posteriores se borran pero no los archivos.

**git reset --hard id**
Por ejemplo *git reset --hard 860s5s2* el HEAD esta apuntando a ese commit y los commits posteriores se han eliminado como tambien los cambios que contenian. Para cuando cometimos errores y queremos volver al pasado.

**git reflog**
Historial de todos los commits resets..

**git reset --hard id**
Volvemos a un punto de la historia con el id que querramos. Y todos los archivos vuelven.

**git mv nombre-actual.txt nuevo-nombre.txt**
Renombrar un archivo. *git status -sb* muestra R en verde los que se han renombrado

**git rm archivo.tst**
Elimina un archivo y podemos confirmarlo para saber en que momento eliminamos el archivo.

**.gitignore**
En este archivo se apunto todo lo que queremos que git ignore por ejemplo la carpeta node_modules.

## Ramas
Es una linea de tiempo de commits.

**Merge**
Uniones:
    - Fast-forward
    - Uniones automaticas
    - Manual

**git branch nombre-de-la-rama**
Creamos una nueva rama.

**git branch**
Indica las ramas existentes y marca de verde la rama en la se esta trabajando.

**git checkout nombre-de-la-rama**
Cambiamos a esa rama. Nuestro HEAD apuntara a esta rama.

**git merge nombre-de-la-rama**
Juntamos esta rama a la de master, para ello necesitamos estar en la rama master.

**git branch -d nombre-de-la-rama**
Ya ocupada la rama la debemos borrar para ello es -d de delete

**git checkout -b nombre-de-la-rama**
Otra forma de crear y cambiarnos a ella. Dos en uno.

## Tags Etiquetas
Son como versiones del proyecto. Los cuales pueden ser descargados y ver como estaba en ese momento.

**git tag nombre-del-tag**
Creacion de un tag

**git tag**
Muestra  todos los tags que tenemos.

**git tag -d nombre-del-tag**
Eliminamos el tag.

**git tag -a v1.0.0 -m "Mensaje"**
Creacion de un tag de forma completa. -a es el nombre del tag y-m el mensaje.

**git tag -a v1.0.0 id -m "Mensaje"**
id o hash por ejemplo *git tag -a v1.0.0 354d5fe -m "Mensaje"*
Hacemos referencia a algun tag del pasado y alli creamos un tag.

**git show nombre-del-tag**
Por ejemplo *git show v1.0.0* nos muestra detalles de ese tag.

## Git Stash y Git Rebase
### Stach 

**git stage**
Guarda el trabajo realizado hasta ese punto.
Si damos *git status* nos lo muestra limpio y los cambios en lo habiamos estado trabajamdo se borran temporalmente. Si hacemos *git log --oneline --decorate --all --graph* nos mostrara en color rosa (refs/stash) WIP on master (Work in progress)

**git stash list**
Muestra todos los stash, se puede tener muchos stashes.

**git stash pop**
Recuperamos los cambios del stash. Y elimina este del stash.

**git stash drop**
Eliminamos el stash, suele quedarse alli cuando resolvemos conflictos al salvarlo.

## Github

**git push origin master**
Enviamos nuestras confirmaciones locales al remoto.

**git push --tags**
Los tags no se suben por defecto. Este es el comando que los sube.

**git remote -v**
Nos muestra el repositorio remoto en el que estamos.

**git pull -u**
Bajamos los cambios que otros han realizado.

**git clone https://github.com/..**
Clonamos el repositorio del enlace.

**git fetch**
Trae los cambios del repositorio remoto pero a otra rama.

*git pull combina  git fetch+ git merge*
