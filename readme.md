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





