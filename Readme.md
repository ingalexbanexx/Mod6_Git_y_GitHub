### Publicación en GitHub Pages
Subí la carpeta del proyecto a un repositorio nuevo y seleccioná `Settings → Pages → Deploy from a branch → main → /(root)`.
### Entregable Modulo 6 de Git y GitHub
#### Preparar el Entregable
- Abrimos VSCode y una carpeta vacia del Pre-Entregable 6
- Abrimos terminal de VSCode
- Instalamos Git Bash
#### Clonamos y comprobamos historial del Proyecto del Repositorio de GitHub
- Clonamos el repositorio con git clone https://github.com/ingalexbanexx/Mod5-Pseudoclases-y-Bootstrap.git
- Luego entramos a la carpeta con cd Mod5-Pseudoclases-y-Bootstrap
- Verificamos el branch del proyecto con: Git Branch con el resultado: \* main
- Verificamos el historial de proyecto: con GIt Status sobre el branch principal (Main)
  On branch main
  Your branch is up to date with 'origin/main'.
  Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
  modified: README.md
  modified: images/08-20- ALEXBANEXX.png
  modified: images/footer-circuit.jpg
  modified: images/foto-perfil.png
  modified: images/header-circuit.jpg
  no changes added to commit (use "git add" and/or "git commit -a")
- Con git log --oneline
  comprobamos el historial, con el resultado: 1f75807 (HEAD -> main, origin/main, origin/HEAD) Primer commit del proyecto
- git remote -v: Comprobamos a que repositorio apunta
  origin https://github.com/ingalexbanexx/Mod5-Pseudoclases-y-Bootstrap.git (fetch)
  origin https://github.com/ingalexbanexx/Mod5-Pseudoclases-y-Bootstrap.git (push)
- ls: revisamos los archivos del repositorio
  Directorio: G:\Mi unidad\2026- CURSOS\CODERHOUSE - FULL STACK DEVELOPMENT\MODULO 6- GIT Y GITHUB\2026-09-23- ENTREGABLE GIT & GITHUB\Mod5-Pseudoclases-y-Bootstrap
Mode LastWriteTime Length Name
d----- 19/10/2026 13:50 css  
d----- 19/10/2026 13:50 images  
d----- 19/10/2026 13:50 pages  
------ 19/10/2026 16:37 3083 README.md  
------ 19/10/2026 13:50 12197 index.html
#### Creamos el repositorio en GitHub y subimos el repositorio original, prepara para revisar que editar:
- git init: 
Initialized empty Git repository in G:/Mi unidad/2026- CURSOS/CODERHOUSE - FULL STACK DEVELOPMENT/MODULO 6- GIT Y GITHUB/2026-09-23- ENTREGABLE GIT & GITHUB/Mod6_Pseudoclases_y_Bootstrap_Git/.git/
- git branch -m main: Cambiar de nombre a la rama principal (antes master)
- git status
On branch master
No commits yet
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        css/
        images/
        index.html
        pages/
nothing added to commit but untracked files present (use "git add" to track)
- git add .: (staging) añade archivos al área de preparación

- git add .: agregamos el proyecto al staging para poder trabajarlos
- git commit -m " Preparacion y revision de archivos para generar ramas de modificaciones ":
[main (root-commit) b018048] Preparación para revisión de los archivos para los cuales vamos a generar ramas de  modificar
 16 files changed, 2180 insertions(+)
  create mode 100644 css/styles.css
 create mode 100644 images/ALEXBANEXX.png
 create mode 100644 images/favicon.png
 create mode 100644 images/footer-circuit.jpg
 create mode 100644 images/foto-perfil.png
 create mode 100644 images/header-circuit.jpg
 create mode 100644 images/hero-workspace.svg
 create mode 100644 images/logo-alexbanexx.png
 create mode 100644 images/project-commerce.svg
 create mode 100644 images/project-dashboard.svg
 create mode 100644 images/project-institutional.svg
 create mode 100644 index.html
 create mode 100644 pages/contacto.html
 create mode 100644 pages/proyectos.html
 create mode 100644 pages/servicios.html
 create mode 100644 pages/sobre-mi.html
- git log –oneline: a8747f6 (HEAD -> master) Preparacion y revision de archivos para generar ramas de modificaciones
- git remote add origin https://github.com/ingalexbanexx/Mod6_Git_y_GitHub.git: Nos conectamos al repositorio remoto.
- git push -u origin main
Enumerating objects: 22, done.
Counting objects: 100% (22/22), done.
Delta compression using up to 8 threads
Compressing objects: 100% (21/21), done.
Writing objects: 100% (22/22), 3.41 MiB | 1.54 MiB/s, done.
Total 22 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), done.
To https://github.com/ingalexbanexx/Mod6_Git_y_GitHub.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

#### Creamos los Branches (ramas) y hacemos las modificaciones
- Rama 1 — Header unificado: feature/header-unificado
Objetivo: unificar logo, nombre, navbar y redes sociales.
•	Logo y nombre AlexBanexx Soluciones IT.
•	Navegación coherente en las cinco páginas.
•	Enlaces de Facebook, Instagram, WhatsApp y correo.
•	Estilos compartidos entre header y footer, respetando la identidad visual tecnológica.
•	Verificación de rutas y menú hamburguesa
Código:
- git checkout feature/header-unificado
Switched to branch 'feature/header-unificado'
- git branch
* feature/header-unificado
  main
Realizamos los cambios en el header, específicamente en la sección NAV-para unificar en las otras pages.
- git add .
- git commit -m "Cambiamos el codigo de NAV en todas las pages igual a Index.htnl"
[feature/header-unificado d5ab712] Cambiamos el codigo de NAV en todas las pages igual a Index.htnl
 4 files changed, 372 insertions(+), 88 deletions(-)
Realizamos las modificaciones del archivo .CSS para estilar las modificaciones del Header
- git add .
- git commit -m "Agregamos al final unas moficiaciones en styles.css para los estilos de la unificacion del Header"
[feature/header-unificado 552e2c2] Agregamos al final unas moficiaciones en styles.css para los estilos de la unificacion del Header
 6 files changed, 293 insertions(+), 17 deletions(-)


- Rama 2 - Mapas de ubicación: feature/mapas-ubicacion
Objetivo: incorporar dos mapas con distribuciones específicas.
En index.html:
•	Sección «¿TENÉS UN PROYECTO?».
•	Texto y botón «Contactarme» agrupados verticalmente.
•	Mapa a la derecha en escritorio.
En pages/contacto.html o el archivo real de contacto:
•	Sección «Hablemos».
•	Mapa a la izquierda del formulario.
•	Formulario a la derecha en escritorio.
En móviles, ambas distribuciones se apilarán verticalmente.
Código:
Creamos la Rama 2 y nos posicionamos en ella
- git switch -c feature/mapas-ubicacion                               
Switched to a new branch 'feature/mapas-ubicacion'
- git branch
  feature/header-unificado
* feature/mapas-ubicacion
  main
Hacemos las modificaciones de la incorporación de los mapas
Primero en el Index.html
-  git add .
- git commit -m "Incluir el mapa de ubicacion en index.html en la seccion al final del main"
[feature/mapas-ubicacion 4839403] Incluir el mapa de ubicacion en index.html en la seccion al final del main
 1 file changed, 45 insertions(+), 7 deletions(-)
Segundo en contacto.html
- git add
- git commit -m "Incluir el mapa de ubicacion en contacto.html en la seccion al final del main al lado del formulario"
[feature/mapas-ubicacion 3572bb3] Incluir el mapa de ubicacion en contacto.html en la seccion al final del main al lado del formulario
 1 file changed, 205 insertions(+), 161 deletions(-)
Hacemos las modificaciones en el archivo styles.css para dos cosas, incluir mapas y responsividad
- git add .
- git commit -m "Agregamos las modificaciones al final del archivo styles.css para estilizar la insercion de los mapas de ubicacion"
[feature/mapas-ubicacion 5993085] Agregamos las modificaciones al final del archivo styles.css para estilizar la insercion de los mapas de ubicacion
 1 file changed, 212 insertions(+) 

- Rama 3 - Documentación README: docs/readme-proyecto
Objetivo: documentar el proyecto y su evolución.
•	Descripción general y objetivos.
•	Tecnologías, estructura y páginas.
•	Cambios implementados en cada rama.
•	Identidad visual, navbar, redes sociales y mapas.
•	Mejoras responsivas y pruebas.
•	Historial de commits.
•	Enlaces al repositorio y al sitio desplegado.
Código:
Creamos la rama 3 y nos posicionamos en ella
 - git switch -c docs/readme-proyecto                                  
Switched to a new branch 'docs/readme-proyecto
- t> git branch
* docs/readme-proyecto
  feature/header-unificado
  feature/mapas-ubicacion
  main
Creamos el archivo readme.md y añadimos el contenido con lo solicitado
- git add .
- git commit -m "Creacion del Readme.md y agregamos el contenido con lo solicitado en la consigna"
[docs/readme-proyecto 87bad24] Creacion del Readme.md y agregamos el contenido con lo solicitado en la consigna
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 Readme.md
Realizo una revisión del log de movimientos en una línea, como historial de commits
- git log --oneline
87bad24 (HEAD -> docs/readme-proyecto) Creacion del Readme.md y agregamos el contenido con lo solicitado en la consigna
5993085 (feature/mapas-ubicacion) Agregamos las modificaciones al final del archivo styles.css para estilizar la insercion de los mapas de ubicacion
3572bb3 Incluir el mapa de ubicacion en contacto.html en la seccion al final del main al lado del formulario
4839403 Incluir el mapa de ubicacion en index.html en la seccion al final del main
552e2c2 (feature/header-unificado) Agregamos al final unas moficiaciones en styles.css para los estilos de la unificacion del Header
d5ab712 Cambiamos el codigo de NAV en todas las pages igual a Index.htnl
a8747f6 (origin/master, origin/main, origin/HEAD, main) Preparacion y revision de archivos para generar ramas de modificaciones
Terminamos la edición del Archivo Readme.md, después de los merge, subimos el link del repositorio al sitio desplegable
- git add .
- git commit -m “Terminamos de editar el archivo Readme.md antes de los merge con las todas las ramas”
