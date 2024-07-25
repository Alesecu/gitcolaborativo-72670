# Clase 02 - Git Desarrollo Colaborativo

![Git-Github](_ref/git-github.png)

## Repaso de comandos para realizar persistir los cambios de archivos dentro del repositorio

```sh
git status
```

## GIT COMMIT: Para persistir los cambios 
Los archivos elegimos y colocados en el Staging Area vamos a querer persistirlos.

```sh
git commit -m "Mensaje descriptivo de lo que estoy guardando dentro del commit"
```

## Corregir un commit (tanto el mensaje como el contenido)

```sh
git add <nombre-archivo>
git commit --amend
```

## Visualizar el timelime de los commits (instaneas/snapshot)

```sh
git log # versión larga 
git log --oneline # versión corta
git log --oneline -2 # ver una cantidad limitada de commits 
```
Nota: Para salir de la aplicación 'less' tengo que aprentar la tecla 'q' -> quit 
