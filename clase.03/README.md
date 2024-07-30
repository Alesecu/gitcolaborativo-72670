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







