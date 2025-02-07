#Usando Repositorios

    REPOSITORIO: DESDE MI NOTE (REPO LOCAL) A GITHUB (REPO REMOTO)
    Pasos para subir repositorio a github desde uno creado en local server

      git init //en terminal git bash desde vscode

      git add . // o git add archivo.html (usar . manda a staging todos los archivos)

      git commit -m "first commit" //o cualquier comentario ad hoc para el cambio hecho

    - Ir a github.com -> new (para crear nuevo repositorio)
    - Sin readme.md
    - Crear
    - Volver a vscode
    - En bash:

      git remote add origin https://github.com/camilahurtadoc/nombre-repositorio.git

      git branch -M main

      git push -u origin main

    - Ahora debería mostrar un enumerating, counting, etc etc en el bash y terminar con
        * [new branch]      main -> main
        branch 'main' set up to track 'origin/main'. 
    - Ahora quedó linkeado el repositorio
    - Cada vez que haga cambios, tengo que llevar a staging (git add .) y 
    commitear (git commit) para ir actualizando los cambios en el repositorio.
    - Para subir los cambios de vuelta al servidor remoto (github) tengo q hacer

      git push origin main
    

--------------------------------------------------------------------------------


    REPOSITORIO: DESDE FORK EN GITHUB (REPO REMOTO) A MI NOTE (REPO LOCAL)
    Instrucciones para hacer el fork
    - En github.com, en el repositorio q quiera forkear, lo forkeo
    - Tengo que clonar este repo del servidor remoto (q acabo de ofrkear) a mi servidor local
    - Voy al repo forkeado (en mis repositorios), a < > Code (botón verde)
    - Local -> SSH -> copiar link (git@github.com:camilahurtadoc/nombre-repo-forkeado.git)
    - Volver a vscode, en git bash
    - Verificar que estoy en la carpeta donde quiero dejar el repositorio (en mi note)
    - Pegar link agregando git clone en bash:

      git clone git@github.com:camilahurtadoc/nombre-repo-forkeado.git

    - Si pide verificar origen de confianza (Y,n), poner Y (en mayúscula)
    - Si quedó bien hecho, debería decir (main) en el bash, en la carpeta
    - No es necesario usar git init, viene listo si fue forkeado
    - Entrar a carpeta de repo forkeado en servidor local, en vscode terminal git bash

      cd nombre-repo-forkeado

    - Editar archivos usando vscode
    - Para guardar cambios y subir, lo mismo q antes: add, commit y push para subir

      git add .

      git commit -m "cambios hechos"

      git push origin main //para subir los cambios del servidor local al remoto

    - Verificar en github.com q se subieron los cambios hechos en vscode