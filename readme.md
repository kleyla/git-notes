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

