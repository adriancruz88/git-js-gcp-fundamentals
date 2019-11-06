# Fundamentos de GIT

## Historia

[HISTORIA DOCUMENTACIÓN](https://git-scm.com/book/es/v1/Empezando-Una-breve-historia-de-Git)

Como muchas de las grandes cosas en esta vida, Git comenzó con un poco de destrucción creativa y encendida polémica. El núcleo de Linux es un proyecto de software de código abierto con un alcance bastante grande. Durante la mayor parte del mantenimiento del núcleo de Linux (1991-2002), los cambios en el software se pasaron en forma de parches y archivos. En 2002, el proyecto del núcleo de Linux empezó a usar un DVCS propietario llamado BitKeeper.

En 2005, la relación entre la comunidad que desarrollaba el núcleo de Linux y la compañía que desarrollaba BitKeeper se vino abajo, y la herramienta dejó de ser ofrecida gratuitamente. Esto impulsó a la comunidad de desarrollo de Linux (y en particular a Linus Torvalds, el creador de Linux) a desarrollar su propia herramienta basada en algunas de las lecciones que aprendieron durante el uso de BitKeeper. Algunos de los objetivos del nuevo sistema fueron los siguientes:

Velocidad
Diseño sencillo
Fuerte apoyo al desarrollo no lineal (miles de ramas paralelas)
Completamente distribuido
Capaz de manejar grandes proyectos (como el núcleo de Linux) de manera eficiente (velocidad y tamaño de los datos)

![LINUS TORVALDS](assets/linus_torvalds.jpg)

## GIT

[DOCUMENTACIÓN FUNDAMENTOS](https://git-scm.com/book/es/v1/Empezando-Fundamentos-de-Git)

Entonces, ¿qué es Git en pocas palabras? Es muy importante asimilar esta sección, porque si entiendes lo que es Git y los fundamentos de cómo funciona, probablemente te sea mucho más fácil usar Git de manera eficaz. A medida que aprendas Git, intenta olvidar todo lo que puedas saber sobre otros VCSs, como Subversion y Perforce; hacerlo te ayudará a evitar confusiones sutiles a la hora de utilizar la herramienta. Git almacena y modela la información de forma muy diferente a esos otros sistemas, a pesar de que su interfaz sea bastante similar; comprender esas diferencias evitará que te confundas a la hora de usarlo.

## FLUJO DE TRABAJO EN GIT

La principal diferencia entre Git y cualquier otro VCS (Subversion y compañía incluidos) es cómo Git modela sus datos. Conceptualmente, la mayoría de los demás sistemas almacenan la información como una lista de cambios en los archivos. Estos sistemas (CVS, Subversion, Perforce, Bazaar, etc.) modelan la información que almacenan como un conjunto de archivos y las modificaciones hechas sobre cada uno de ellos a lo largo del tiempo.

![GIT CYCLE](assets/git-cycle.png)

## GIT FLOW

Gitflow Workflow es un diseño de flujo de trabajo Git que se publicó por primera vez y se hizo popular por Vincent Driessen en nvie . El flujo de trabajo de Gitflow define un modelo de ramificación estricto diseñado en torno al lanzamiento del proyecto. Esto proporciona un marco robusto para gestionar proyectos más grandes.

### ¿Cómo funciona?

1.

En lugar de una sola rama master, este flujo de trabajo usa dos ramas para registrar el historial del proyecto. La rama master almacena el historial de lanzamientos oficiales, y la rama develop sirve como una rama de integración de nuevas características.

![GIT FLOW 1](assets/flow1.svg)

2.

Cada nueva característica debe residir en su propia rama, que se puede enviar al repositorio central para respaldo/colaboración. Pero, en lugar de ramificarse sobre master, las ramas 'features' usan develop como su rama principal. Cuando se completa una característica, se deben fusionar nuevamente con la rama develop . Las características nunca deberían interactuar directamente con master.

![GIT FLOW 2](assets/flow2.svg)

3.

Una vez que en la rama develop han ocurrido suficientes modificaciones para un lanzamiento (o se acerca una fecha de lanzamiento predeterminada). Se bifurca una rama release que nade de la rama develop. La creación de esta rama inicia el siguiente ciclo de lanzamiento, por lo que no se pueden agregar nuevas características después de este punto, solo las correcciones de errores, la generación de documentación y otras tareas orientadas a la versión deben ir en esta rama.

![GIT FLOW 3](assets/flow3.svg)

4.

El mantenimiento o las ramas “hotfix” se utilizan para parchear rápidamente las versiones de producción.

![GIT FLOW 3](assets/flow4.svg)

## LISTA DE COMANDOS PARTE 1

- **git init** - Este comando se usa para crear un nuevo repositorio GIT (inicializa GIT en el proyecto).
- **git add** - Este comando puede ser usado para agregar archivos a la stagin area

Agregar archivos de forma interactiva

git add -i

- **git status** - Este comando muestra la lista de los archivos que se han cambiado junto con los archivos que están por ser añadidos o comprometidos.
- **git branch** - Este comando se usa para listar, crear o borrar ramas (git branch -d )
- **git reset** - El comando se usa para resetear la staging área y el directorio que está trabajando al último estado comprometido.
