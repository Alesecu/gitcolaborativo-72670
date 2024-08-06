# Clase 05 - Git Desarrollo Colaborativo

## Gist
Compartir código, pasar snippet a otras personas o información que quiero compartir. Pueden tener varios archivos y sus revisiones

<https://gist.github.com/>

* Secretos -> Solo la persona que tenga el link va a poder verlo. No son privados. 
* Públicos -> Se van indexar en los motores de búsqueda

## Proyectos
Son tableros visuales tipo Kanban donde podemos organizar y visualizar el progreso de nuestras tareas asociar tareas a resolución de issues.

## Issues (Posibles problemas, solución de temas)
Nos permiten tener un seguimiento sobre posibles bugs o errores en nuestras aplicaciones.

## Trabajando con colaboradores
Cuando yo conozco a las personas que van a trabajar conmigo puedo agrearlos al repositorio en el cual quiero trabajar para ellos puedan acceder y trabajar como si ellos también fueran dueños del repositorio.

## Git Blame
Me va a permitir ver línea por línea quien fue el último que modificó esa línea y en que commit se hizo el cambio.

```sh
git blame <nombre-archivo>
git blame <nombre-archivo> -L # rango de líneas
git blame <nombre-archivo> -e o -s # correo o nombre del que hizo el commit
```

```sh
git blame --help
```

## Trabajar colaborativamente con personas que no conozco (Fork y Pull Request)

Me permite trabajar colaborativamente en proyectos donde no conozco a las personas o no tengo la suficiente confianza para darle permisos al repositorio de trabajo. 

Normalmente cuando trabajo con Fork y Pull Request lo hago en proyectos Open Source.

* Fork es una copia del respositorio remoto de alguien a mi cuenta de GitHub.
* Pull Request. Solicitud  a los dueños originales del repositorio para proponerles un cambio. Es una propuesta de cambio a alguien que no conozco pero quiero ayudar.

1. Hacer un fork del proyecto. Del proyecto del cual quiero contribuir (Me voy copiar en mi cuenta el repo del proyecto original)
2. Me clono el fork desde mi cuenta github
3. Trabajo normalmente. Subo los cambios (A repo propio)
4. Me voy al proyecto original en el apartado Pull Request. Creo un nuevo Pull Request. Algunas veces aparece en mi repo la posibilidad Pull Request.
---
5. Si el repo original sufrió más modificaciones. (Commits). Voy a tener que actualizar mi fork.
6. Voy a la cuenta del proyecto original y me copio la url del repositorio
7. Y agrego en mi repositorio local, la url (el remoto) del proyecto original.

    git remote add upstream <URL-repositorio-original>

8. Me traigo los cambios del repositorio original a mi repo local

    git pull upstream <rama-que-quiero-actualizar>

9. Subo a mi repositorio remoto (Fork) las actualizaciones del repo local

    git push origin <rama-a-actualizar>












