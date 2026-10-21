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

#### Realizamos los Merges con todas las Ramas
Verificamos el estado antes de integrar
- git status
- git branch -avv
- git remote -v
On branch docs/readme-proyecto
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   Readme.md
* docs/readme-proyecto     cfc04d4 Terminamos de editar el archivo Readme.md antes de los merge con todas las ramas
  feature/header-unificado 552e2c2 Agregamos al final unas moficiaciones en styles.css para los estilos de la unificacion del Header
  feature/mapas-ubicacion  5993085 Agregamos las modificaciones al final del archivo styles.css para estilizar la insercion de los mapas de ubicacion
  main                     a8747f6 [origin/main] Preparacion y revision de archivos para generar ramas de modificaciones
  remotes/origin/HEAD      -> origin/master
  remotes/origin/main      a8747f6 Preparacion y revision de archivos para generar ramas de modificaciones
  remotes/origin/master    a8747f6 Preparacion y revision de archivos para generar ramas de modificaciones
origin  https://github.com/ingalexbanexx/Mod6_Git_y_Github.git (fetch)
origin  https://github.com/ingalexbanexx/Mod6_Git_y_Github.git (push)

Vamos a integrar los cambios en el orden correcto, entonces primero actualizamos la rama principal “main”
- git switch main
- git pull --ff-only origin main: evitamos que Git cree merge adicionales innecesarios
From https://github.com/ingalexbanexx/Mod6_Git_y_Github
 * branch            main       -> FETCH_HEAD
Already up to date.
- git branch
  docs/readme-proyecto
  feature/header-unificado
  feature/mapas-ubicacion
* main
Incorporamos los commits del encabezado a main
- git merge --ff-only feature/header-unificado
Updating a8747f6..552e2c2
error: Your local changes to the following files would be overwritten by merge: css/styles.css
Please commit your changes or stash them before you merge.
Aborting
Me da un error por el archivo styles.css, entonces, buscamos soluciones 
- git add css/styles.css
- git commit -m "Estilos locales actualizados"
On branch main
Your branch is up to date with 'origin/main'.
nothing to commit, working tree clean
Hacemos la integración de la rama feature/header-unificado con éxito.
- git merge --ff-only feature/header-unificado
Updating a8747f6..552e2c2
Fast-forward
 css/styles.css       | 276 +++++++++++++++++++++++++++++++++++++++++++++++++++
 index.html           |   2 +-
 pages/contacto.html  | 139 +++++++++++++++++---------
 pages/proyectos.html | 107 +++++++++++++++++---
 pages/servicios.html | 107 +++++++++++++++++---
 pages/sobre-mi.html  | 107 +++++++++++++++++---
 6 files changed, 649 insertions(+), 89 deletions(-)
- git commit -m "Integramos correctamente la rama feature/header-unificado y subimos los cambios al proyecto remoto"
On branch main
Your branch is up to date with 'origin/main'.
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   css/styles.css
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Readme.md
no changes added to commit (use "git add" and/or "git commit -a")
Tenemos problemas con la integración de la rama adecuadamente a main, solucionamos
- git add .
- git commit -m "Integramos correctamente la rama feature/header-unificado y subimos los cambios al proyecto remoto"
[main 3921bf1] Integramos correctamente la rama feature/header-unificado y subimos los cambios al proyecto remoto
 1 file changed, 188 insertions(+)
 create mode 100644 Readme.md
- git push origin main
>> Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 3.51 KiB | 224.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: This repository moved. Please use the new location:
remote:   https://github.com/ingalexbanexx/Mod6_Git_y_GitHub.git
To https://github.com/ingalexbanexx/Mod6_Git_y_Github.git
   552e2c2..3921bf1  main -> main
PS G:\Mi unidad\2026- CURSOS\CODERHOUSE - FULL STACK DEVELOPMENT\MODULO 6- GIT Y GITHUB\2026-09-23- ENTREGABLE GIT & GITHUB\Mod6_Pseudoclases_y_Bootstrap_Git> git status
On branch main
Your branch is up to date with 'origin/main'.
nothing to commit, working tree clean
- git status
On branch main
Your branch is up to date with 'origin/main'.
nothing to commit, working tree clean
Verificamos que todo este bien, y corroboramos que el repositorio tiene un estado ideal
- git log --oneline --decorate -5
>> git status
3921bf1 (HEAD -> main, origin/main) Integramos correctamente la rama feature/header-unificado y subimos los cambios al proyecto remoto
552e2c2 (feature/header-unificado) Agregamos al final unas moficiaciones en styles.css para los estilos de la unificacion del Header
d5ab712 Cambiamos el codigo de NAV en todas las pages igual a Index.htnl
a8747f6 (origin/master, origin/HEAD) Preparacion y revision de archivos para generar ramas de modificaciones
On branch main
Your branch is up to date with 'origin/main'.
nothing to commit, working tree clean
Ahora integramos la rama de los mapas de ubicación, feature/mapa-ubicación
- git merge --ff-only feature/mapas-ubicacion
hint: Diverging branches can't be fast-forwarded, you need to either:
hint:
hint:   git merge --no-ff
hint:
hint: or:
hint:
hint:   git rebase
hint:
hint: Disable this message with "git config set advice.diverging false"
fatal: Not possible to fast-forward, aborting.
Da un error el cual solucionamos de la siguiente forma, solucionamos todos los inconvenientes.
- git merge feature/mapas-ubicacion
>> 
Merge made by the 'ort' strategy.
 css/styles.css      | 212 ++++++++++++++++++++++++++++++
 index.html          |  52 +++++++-
 pages/contacto.html | 366 +++++++++++++++++++++++++++++-----------------------
 3 files changed, 462 insertions(+), 168 deletions(-)
- git push origin main
>> 
Enumerating objects: 25, done.
Counting objects: 100% (20/20), done.
Delta compression using up to 8 threads
Compressing objects: 100% (12/12), done.
Writing objects: 100% (13/13), 4.83 KiB | 126.00 KiB/s, done.
Total 13 (delta 6), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (6/6), completed with 4 local objects.
remote: This repository moved. Please use the new location:
remote:   https://github.com/ingalexbanexx/Mod6_Git_y_GitHub.git
To https://github.com/ingalexbanexx/Mod6_Git_y_Github.git
   3921bf1..91efd1b  main -> main
Renombramos el Repositorio remoto ya que aparentemente se modifico su nombre
- git merge feature/mapas-ubicacion -m "Fusionamos la rama de mapas de ubicacion"
>> 
Already up to date.
- git remote -v
>> 
origin  https://github.com/ingalexbanexx/Mod6_Git_y_GitHub.git (fetch)
origin  https://github.com/ingalexbanexx/Mod6_Git_y_GitHub.git (push)
Ahora integramos la rama de docs/readme-proyecto
- git merge docs/readme-proyecto -m "Fusionamos la rama de documentacion docs/readme-proyecto"
>> 
Merge made by the 'ort' strategy.
- git push origin main
>> 
Enumerating objects: 11, done.
Counting objects: 100% (11/11), done.
Delta compression using up to 8 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (8/8), 1.02 KiB | 52.00 KiB/s, done.
Total 8 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), completed with 2 local objects.
To https://github.com/ingalexbanexx/Mod6_Git_y_GitHub.git
   91efd1b..69d7817  main -> main

Historial de Commits
- git log --oneline
69d7817 (HEAD -> main, origin/main) Fusionamos la rama de documentacion docs/readme-proyecto
91efd1b Merge branch 'feature/mapas-ubicacion'
3921bf1 Integramos correctamente la rama feature/header-unificado y subimos los cambios al proyecto remoto
be1fdec (docs/readme-proyecto) Seguimos editando Redmi.md con contenido nuevo, antes de la integracion general
cfc04d4 Terminamos de editar el archivo Readme.md antes de los merge con todas las ramas
87bad24 Creacion del Readme.md y agregamos el contenido con lo solicitado en la consigna
5993085 (feature/mapas-ubicacion) Agregamos las modificaciones al final del archivo styles.css para estilizar la insercion de los mapas de ubicacion
3572bb3 Incluir el mapa de ubicacion en contacto.html en la seccion al final del main al lado del formulario
4839403 Incluir el mapa de ubicacion en index.html en la seccion al final del main
552e2c2 (feature/header-unificado) Agregamos al final unas moficiaciones en styles.css para los estilos de la unificacion del Header
d5ab712 Cambiamos el codigo de NAV en todas las pages igual a Index.htnl
a8747f6 (origin/master, origin/HEAD) Preparacion y revision de archivos para generar ramas de modificaciones

Link del repositorio y el sitio desplegado
Repositorio y Despliegue del Sitio: https://github.com/ingalexbanexx/Mod6_Git_y_GitHub.git  


