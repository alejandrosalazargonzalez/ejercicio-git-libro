# ejercicio-git-libro

## Clono el repositorio
```code
    git clone https://github.com/alejandrosalazargonzalez/ejercicio-git-libro.git
Clonando en 'ejercicio-git-libro'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Recibiendo objetos: 100% (3/3), listo.

    ls -la
total 16
drwxrwxr-x 3 bae2 bae2 4096 oct 10 18:01 .
drwxr-xr-x 7 bae2 bae2 4096 oct 10 18:01 ..
drwxrwxr-x 8 bae2 bae2 4096 oct 10 18:01 .git
-rw-rw-r-- 1 bae2 bae2   21 oct 10 18:01 README.md
```
## Ejercicio 1
### Ejecuto el comando log
```code
    git log
commit 6b20ec1667976c5a0897caeb91f84b60b49734f8 (HEAD -> main, origin/main, origin/HEAD)
Author: Salazar <115075962+alejandrosalazargonzalez@users.noreply.github.com>
Date:   Thu Oct 10 18:01:20 2024 +0100

    Initial commit
```
### Creo la carpeta capitulos y el archivo "capitulo1.txt"
```code
    mkdir capitulos

    Git es un sistema de control de versiones ideado por Linus Torvalds.
```