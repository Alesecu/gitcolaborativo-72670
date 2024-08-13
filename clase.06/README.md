# Clase 06 - Git Desarrollo Colaborativo

# GIT TAG
Son referencias que apunta a puntos especificos en el historial del repositorio (A hashes especificos)

```sh
git tag <nombre-etiqueta> # Etiqueta ligera (lightweight tags) -> Solo es un identificador, no almecana info adicional.
git tag -a <nombre-etiqueta> -m "Mensaje descriptivo de tag" # Etiqueta anotada
```

> Etiqueta ligera

```sh
git tag son-una-etiqueta-ligera
```

> Etiqueta anotada

```sh
git tag -a v0.0.1 <hash> -m "Esta es la primera versión de nuestra aplicación"
git tag -a v0.0.1 78279b9 -m "Esta es la primera versión de nuestra aplicación"
```

## Listar Tags

```sh
git tag -l
```

## Como eliminar un tag

```sh
git tag -d <nombre-tag>
```

## Mostrar la info de la etiqueta

```sh
git show <nombre-tag>
```

## Compartir un tag -> Subirlo a nuestro repo remoto

```sh
git push origin --tags # NO USAR -> Subir todos los tags
```

```sh
git push origin <nombre-etiqueta>
git push origin v0.0.1
git push origin v0.1.2
git push origin v1.0.0
```

# GIT RESTORE
Me permitwe descartar cambios en el directorio de trabajo o área de staging área. Nos permite revertir archivos a un estado anterior.

```sh
git restore . <nombre-archivo>
git restore --source=HEAD <nombre-archivo>
git restore --source=HEAD clase.02/README.md # Ejemplo
```

## Recuperar una versión anterior del archivo

```sh
git restore --source=<hash> clase.02/README.md
git restore --source=fd1a2 clase.02/README.md
```
## Recuperar todos los archivos en una versión anterior


```sh
git restore --source=fd1a2 *.java
```

## Eliminar archivos del área de preparación (staging area)

```sh
git restore --staged <nombre-archivo>
```

## También puedo restaurar un parte del archivo

```sh
git restore --patch 
```

# GIT REVERT
Me permite deshacer un commit y crear uno nuevo con una versión anterior del archivo/s

## Revierte un commit en particular

```sh
git revert <hash>
```

## Revierte un rango de commit en particular

```sh
git revert <hash>..<hash>
```

## Revierte un commit pero no hace el commit del revert...

```sh
git revert --no-commit <hash>
```

# GIT REBASE
Otro tipo de fusión donde me traigo los cambios (commits) pero esos commits se vuelve hacer creando nuevos hashes

```sh
git rebase <rama>
```

```sh
git switch feature/rebase
git rebase main
# Soluciono conflictos. Y le aviso que puede continuar el rebase
git rebase --continue
git rebase --skip # salto ese conflicto
```

# Aborto el rebase 

```sh
git rebase --abort
```



