## GIT PARTE DOS

### LISTA DE COMANDOS PARTE 2

- **git checkout** - se usa para cambiar de rama y revisar el contenido de tu directorio de trabajo.

- **git reset** - El comando se usa para resetear la staging área y el directorio que está trabajando al último estado comprometido.

git reset --hard origin/master

- **git fetch** - Este comando obtiene todo lo necesario para reconstruir el historial de la rama en particular que le interesa.

git fetch <remote-repo> <remote-branch>
git fetch origin

Lo interesante del comando fetch es que en realidad no afecta nada en su repositorio local. No se perderán cambios de trabajo, y no verá ningún efecto directo en sus sucursales locales. Esto se debe a que Git mantiene el contenido recuperado separado del contenido de su propio repositorio hasta que se fusiona.

- **git merge** - se utiliza para fusionar uno o más ramas dentro de la rama que tienes activa.

- **git mergetool** - resolución de conflictos de fusión para resolver conflictos de fusión.

- **git log** - se utiliza para mostrar la historia registrada alcanzable de un proyecto desde la más reciente instantánea confirmada hacia atrás. Por defecto sólo se mostrará la historia de la rama en la que te encuentres

- **git stash** - se utiliza para almacenar temporalmente el trabajo no confirmado con el fin de limpiar el directorio de trabajo sin tener que confirmar el trabajo no acabado en una rama.

- **git tag** - Se utiliza para dar un marcador permanente a un punto específico en el historial del código fuente. Generalmente esto se utiliza para cosas como las liberaciones (releases).

- **git clone** - Crea una copia local del repositorio ejecutando

Si utilizas un servidor remoto, ejecuta

git clone username@host:/path/to/repository

- **git commit** - git commit guarda una snapshot del stage como un commit
  git commit -a

- **git diff** -

* **git diff --check** - Comando útil para detectar las marcas que se crean cuando se genera un conflicto.
* **git add** - Este comando puede ser usado para agregar archivos a la stagin area
* **git status** - Este comando muestra la lista de los archivos que se han cambiado junto con los archivos que están por ser añadidos o comprometidos.
* **git branch** - Este comando se usa para listar, crear o borrar ramas (git branch -d )

cambio
