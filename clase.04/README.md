# Git Stash

Tiene una estructura de datos tipo pila y me permite guardar cambios que sucedieron en el working o estan en la zona de staging pero no quiero que aún sean un commit.

## Crear un stash

```sh
git stash # git elije el nombre con el que me guarda el stash
git stash -m "Comando para crear un stash"
```

## Listar los stashes

```sh
git stash list
```

## Comparando los stash con una rama.

```sh
git diff stash@{0} dev
```

## Traigo un stash al WD. (Es el último stash)

```sh
git stash pop # Además de traernos la info, borra el stash. Siempre y cuando no haya conflicto.
```

## Traigo un stash especifico al WD.

```sh
git stash apply # el último (No elimina)
git stash apply 4 # traer el stash 4 en particular
```

## Borro un stash

```sh
git stash drop # el último
git stash drop 5 # borra el stash 5 en particular
```

## El ayuda del comando

```sh
git stash --help
```

# Git alias
Me permite crear alias de comandos para en vez de estar escribiendo el comando y sus subcomandos hacerlo directamente con un alias. A traves de una letra o una palabra

## Creando alias

```sh
git config --global alias.<alias-elegido> "<comando-de-git-sin-la-palabra-git>"
git config --global alias.s "status --short"
git config --global alias.c "commit -m"
git config --global alias.l "log --oneline"
git config --global alias.ll "log --oneline --all --graph --decorate"
```

## Quitar alias

```sh
git config --global --unset alias.ll ## me quita el alias ll
```

## Listar los alias configurados

```sh
git config --global --get-regexp alias
```

# Git RESET
Me permite deshacer un commit o commits (cambios) en el repositorio. Los cambios deshechos se van a colocar en el área de trabajo o el área de staging.

## 3 tipos de resets

1. Reset Soft
Va a borrar el commit o los commits seleccinados y arrojar los cambios al staging area

```sh
git reset --soft <hash>
```

2. Reset Mixed
Va a borrar el commit o los commits seleccionados y arrojar el contenido de esos commits dentro de la área Working directory.

```sh
git reset <hash>
git reset --mixed <hash>
```

3. Reset Hard (CUIDADO)
Va a borrar el commit o los commits seleccionados y descargar el contenido. O sea los cambios se pierden.

```sh
git reset <hash>
git reset --hard <hash>
```

# Git Cherry Pick
Permite selecionar un commit o varios de manera independiente y colocars en otra rama.

# Selecciono un único commit 

```sh
git cherry-pick <hash>
```
