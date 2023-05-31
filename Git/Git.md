# Git

Para ver gráficamente como funcionan los comandos hay que ir [aquí](https://git-school.github.io/visualizing-git/#free).

## Comandos

- `git init`: Iniciar repositorio.
- `git diff`: Ver cambios que se han hecho aún cuando no se han preparado para hacer `commit`.
- `git status`: Estatus de los archivos.
- `git status -s`: Lista de estatus de los archivos simplificada.
- `git add .`: Añade **todos los archivos** con cambios a la parte.
- `git add {nombre del archivo}`: Añade **un archivo** en especifico.

## Log

- `git log`: Ver la lista de versiones.
- `git log -p`: Ver lista de cambios especificos de cada versión.

## Servidores remotos

- `git init --bare`: Sólo guarda modificaciones de git, no tiene copias de archivos, sólo las modificaciones.
- `git remote`: Busca y enlista servidores remotos.
- `git remote add {nombre del servidor} {ubicación del servidor}`: Añade un servidor remoto.
- `git remote -v`: Muestra a donde apunta el servidor y para verificar que el servidor fue agregado. De donde viene la información (*fetch*), y a donde va (*push*).
- `git clone {ubicación del repositorio}`: Clonar un repositorio.

### Manejo de servidores remotos de Git

- `git push {nombre del repo} {rama}`: (Empujar) Manda los cambios al repositorio remoto.
- `git pull {nombre del repo} {rama}`: (Jalar) Extrae los nuevos cambios realizados desde el repositorio remoto.

## Ramas (Branch)

- `git branch`: Enlista las ramas.
- `git branch {nombre de rama nueva}`: Crear una nueva rama.
- `git checkout {nombre de rama}`: Cambio de rama.
- `git merge {nomdre de rama}`: Fusiona las dos ramas. La rama del nombre en la rama en la que nos encontramos. Se **conserva** la rama que se fusiono.
- `git rebase {nombre de rama}`: Reescribe el historial de una rama, aplicando los cambios directamente sobre otra rama (sobre la que se este al ejecutar el comando) para que parezca que los cambios se hicieron de forma continua.
- `git log --graph`: Ver los cambios comportamiento de las ramas de forma gráfica.

Cuando hay un ***conflicto entre ramas***, lo que sucede es:

- Si se usa `git merge`,Git creará un nuevo commit especial llamado "*commit de fusión*" que **contiene los cambios combinados de ambas ramas**, junto con los marcadores de conflicto que indican las áreas conflictivas del código.
- Si se usa `git rebase`, Git **pausará el rebase cuando encuentre un conflicto y te mostrará las áreas conflictivas** en los archivos correspondientes. Hasta que todos los conflictos se resuelvan.

## Manejo de archivos

- `git restore {nombre de archivo}`: Deshace los cambios realizados antes de que se pase a la etapa de *staged*. Es como un *Ctrl + z*.
- `git restore --staged {nombre de archivo}`: Lo mismo que antes pero ahora el archivo esta en etapa *staged*.
- `git revert {hash de commit}`: Revierte el commit ya realizado. Crea otro commit con la información que tenía el commit anterior al revertido.
