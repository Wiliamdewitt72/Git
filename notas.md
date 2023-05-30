# Git

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
