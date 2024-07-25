# Clase 01 - Git Desarrollor Colaborativo

## Verificando que tenga git instalado

```sh
git --version
```

## Ver si tengo un usario y correo configurado

```sh
git config --get-regexp user
```

## Configuración inicial

```sh
git config --global user.name "Maximiliano Principe"
git config --global user.email mlapeducacionit@gmail.com
```

## Como remover algo que no deseo que este

```sh
git config --global --unset user.mail
```

## Cambiar el editor a nano

```sh
git config --global core.editor nano
```

## Cambiar el nombre por defecto de la rama principal

```sh
git config --global init.defaultBranch main
```

## Ver las configuraciones hechas en un editor 

```sh
git config --global -e
```

## Inicializar un repositorio de GIT

```sh
git init
```

## Para ver las carpetas y archivos ocultos en Linux

```sh
ls -la
```

## Ver el estado de los archivos del proyecto

```sh
git status
```


## Areas posibles en las que pueden estar los archivos

* Working Directory (Directorio de trabajo) donde van agregando, borrando al archivo el desarrolllo

* Staging Area (Area de control de cambios) Se agregan los archivos para darle seguimiento y posteriormente sacarles una foto (commit)

* Local Repo (Area de validación de cambios, donde se registran las modificaciones realizadas) Donde van a estar todas las fotos (commit) que vaya sacando.


## Estados de los archivos

* Untracked (Sin seguimiento) => archivos que no se agregaron al index/stage y por consecuente no se les da seguimiento.
* Staged => Archivos que fueron agregados al index/stage area y cuyos cambios van a ser incorporados al repositorio
* Unmodified => Archivos que se cuentran en en el respositorio y no fueron modificado (Con respecto al repositorio)
* Modified => Archivos que se encuentro en el repositorio pero difieren con lo que se encuentra actualmente en el directorio trabajo (Working directory)
