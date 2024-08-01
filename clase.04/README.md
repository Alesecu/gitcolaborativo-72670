# Git Stash

Tiene una estructura de datos tipo pila y me permite guardar cambios que sucedieron en el working o estan en la zona de staging pero no quiero que aún sean un commit.

## Crear un stash

```sh
git stash # git elije el nombre con el que me guarda el stash
git stash -m "Comando para crear un stash"
```