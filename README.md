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

### Añado los cambios a la zona de intercambios
```code
    git status 
En la rama main
Tu rama está actualizada con 'origin/main'.

Cambios no rastreados para el commit:
  (usa "git add <archivo>..." para actualizar lo que será confirmado)
  (usa "git restore <archivo>..." para descartar los cambios en el directorio de trabajo)
        modificados:     README.md

Archivos sin seguimiento:
  (usa "git add <archivo>..." para incluirlo a lo que será confirmado)
        capitulos/

sin cambios agregados al commit (usa "git add" y/o "git commit -a")

    git add .

    git commit -m "Añadido capitulo 1"
[main 8331191] Añadido capitulo 1
 2 files changed, 35 insertions(+), 1 deletion(-)
 rewrite README.md (100%)
 create mode 100644 capitulos/Capitulo1.txt
```

### ejecuto de nuevo el comando git log
```code
git log
commit 8331191c34c867db20edbca2d6051b36aa5c1368 (HEAD -> main)
Author: alejandrosalazargonzalez <alejandrosalazargonzalez2004@gmail.com>
Date:   Thu Oct 10 18:13:38 2024 +0100

    Añadido capitulo 1

commit 6b20ec1667976c5a0897caeb91f84b60b49734f8 (origin/main, origin/HEAD)
Author: Salazar <115075962+alejandrosalazargonzalez@users.noreply.github.com>
Date:   Thu Oct 10 18:01:20 2024 +0100

    Initial commit
```

## Ejercicio 2
### Creo el Capitulo2.txt
```code
El flujo de trabajo básico con Git consiste en:
 1- Hacer cambios en el repositorio.
 2- Añadir los cambios a la zona de intercambio temporal.
 3- Hacer un commit de los cambios.
```
### Subir los cambios a la zona de intercambio
```code
    git status 
En la rama main
Tu rama está adelantada a 'origin/main' por 2 commits.
  (usa "git push" para publicar tus commits locales)

Cambios no rastreados para el commit:
  (usa "git add <archivo>..." para actualizar lo que será confirmado)
  (usa "git restore <archivo>..." para descartar los cambios en el directorio de trabajo)
        modificados:     README.md

Archivos sin seguimiento:
  (usa "git add <archivo>..." para incluirlo a lo que será confirmado)
        capitulos/Capitulo2.txt

sin cambios agregados al commit (usa "git add" y/o "git commit -a")

    
```
