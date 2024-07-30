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







