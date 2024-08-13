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










