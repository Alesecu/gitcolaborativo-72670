# Clase 03 - Git Desarrollo Colaborativo

## Ramas (Branches)

![estructuras-ramas](_ref/basica.png)

![Alt text](_ref/avanzada.png)

## Creando un rama

```sh
git branch <nombre-rama>
```

## Moverse entre ramas

```sh
git switch <nombre-rama>
git switch feature/ramas
git switch - # Toggle entre las últimas 2 ramas en las que estuve
```

## Para borrar ramas

```sh
git branch -d <nombre-de-la-rama> 
git branch -d feature/ramas # Si no tengo commits dentro de la rama que no fueron fusionados o estan en otra rama. Me va a pedir confirmación de borrado porque si la borra pierdo la información de los commits que no están disponible en las otras ramas
git branch -D feature/ramas
```

## Para ver todas las ramas del proyecto

```sh
git log --oneline --decorate --graph --all
```

## Comparar entre ramas

```sh
git diff <nombre-de-la-rama> # Dependiendo de donde este (O sea en que rama tenga activa) es lo que me va a mostrar el git diff
```

## Git Merge (Fusiones)

Nota: Tengo que estar ubicado en la rama en la cual me quiero traer los cambios. O sea si tengo la rama feature/ramas y quiero traerme los cambios a main. Tengo queestar parado sobre la rama main y ejecutar el siguiente comando.

```sh
git switch main
git merger <nombre-de-la-rama-que-me-quiero-traer-a-main>
git merge feature/ramas
```

## Tipos de fusiones

* Fast-forward: Este tipo de fusión, git lo hace automaticamente
* Tiple vía: Este tipo de fusión, git lo hace automaticamente
* Conflicto: Este tipo de funsión, git no lo puede resolver automaticamente. Lo tenemos que solucionar nosotros.

## Como subir al repositorio remoto una rama

```sh
git push origin <nombre-rama-que-quiero-subir>
git push origin dev
```

## Actualizar la metada que se encuentra en el respositorio remoto

```sh
git fetch
```

## Para listar todas las ramas

```sh
git branch -a
```

## Para que la rama remota se descargué me tengo que mover a la rama

```sh
git switch dev
```


## Clientes de GIT con GUI (Interfaz Gráfica)

* GitHub Desktop <https://github.com/apps/desktop>
* GitKraken <https://www.gitkraken.com/>
* Alternatives <https://alternativeto.net/software/gitkraken/>

## Git Stash
Tiene una estructura de datos tipo pila y me permite guardar cambios que sucedieron en el working o estan en la zona de staging pero no quiero que aún sean un commit.






