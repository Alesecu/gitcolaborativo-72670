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
