# Actualizar nuestro fork con el original

Agregar la referencia al repositorio remoto original, al cual llamaremos «upstream», esto lo logramos con el comando:

```
git remote add upstream https://github.com/whoever/whatever.git
```

Traernos todas las ramas de dicho repositorio remoto con:

```
git fetch upstream
```

Nos vamos a la rama que queremos actualizar, por ejemplo

```
master: git checkout master
```

Reescribir nuestra rama master con los commits nuevos de la rama master del repositorio original con: (No debemos tener cambios sin confirmar)

```
git rebase upstream/master
```

Finalmente si queremos actualizar nuestro fork remoto, lo haremos ejecutando

```
git push -f origin master
```
