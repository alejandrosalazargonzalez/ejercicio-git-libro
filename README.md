# Trabajando con tags, merge entre ramas y reset
## Ejercicio 1: Etiquetar una versión
### Crear etiqueta que marque el estado actual en la rama principal
```code
    git branch 
  bibliografia
* main
  tags
    git tag
1.0.0
1.0.1
```
## Ejercicio 2: Revertir un commit
### Haz un cambio sencillo en uno de los archivos (puedes agregar una línea de texto en el archivo capitulo1.txt), y realiza un commit con un mensaje apropiado, como "Agregada una línea en capítulo 1".
```code
    git status 
En la rama tags
Cambios no rastreados para el commit:
  (usa "git add <archivo>..." para actualizar lo que será confirmado)
  (usa "git restore <archivo>..." para descartar los cambios en el directorio de trabajo)
        modificados:     README.md
        modificados:     capitulos/Capitulo1.txt

sin cambios agregados al commit (usa "git add" y/o "git commit -a")
```
### Muestra el historial de commits
```code
    git log
commit 54d66e76f5bce6ac55249030c4aed681fe249a35 (HEAD -> tags)
Author: alejandrosalazargonzalez <alejandrosalazargonzalez2004@gmail.com>
Date:   Tue Oct 22 23:01:54 2024 +0100

    Revert "Revert "Revert "modifique el readme"""
    
    This reverts commit 86bc59cb6129d1d8487787af5ba32b8771ee3eec.

commit 86bc59cb6129d1d8487787af5ba32b8771ee3eec
Author: alejandrosalazargonzalez <alejandrosalazargonzalez2004@gmail.com>
Date:   Tue Oct 22 22:57:40 2024 +0100

    Revert "Revert "modifique el readme""
    
    This reverts commit b4181b787b61942029e38d03f55b936c2b6ca138.

commit b4181b787b61942029e38d03f55b936c2b6ca138
Author: alejandrosalazargonzalez <alejandrosalazargonzalez2004@gmail.com>
Date:   Tue Oct 22 22:55:47 2024 +0100

    Revert "modifique el readme"
    
    This reverts commit 5d0e48c15a39c4bf3ebfca1df4224cf9feb1ceb0.

commit 5d0e48c15a39c4bf3ebfca1df4224cf9feb1ceb0 (origin/tags)
Author: alejandrosalazargonzalez <alejandrosalazargonzalez2004@gmail.com>
Date:   Tue Oct 22 22:55:14 2024 +0100

    modifique el readme

commit 2c4f64f2940448362f3731c3afb5c0ccb77c4250
Author: alejandrosalazargonzalez <alejandrosalazargonzalez2004@gmail.com>
Date:   Tue Oct 22 22:47:55 2024 +0100

    Agregada una linea en Capitulo1.txt
```

## Ejercicio 3: Aplicar cambios de otra rama con Cherry-pick
### Crea una nueva rama llamada nueva-funcionalidad y haz un cambio en la rama
```code
    git branch nueva-funcionalidad
    git checkout nueva-funcionalidad 
M       README.md
Cambiado a rama 'nueva-funcionalidad'
    git add .
    git commit -m "creo el capitulo 5"
[nueva-funcionalidad 2b98579] creo el capitulo 5
 2 files changed, 45 insertions(+), 1 deletion(-)
 create mode 100644 capitulos/Capitulo5.txt
```
###  usa git cherry-pick
```code
    git checkout tags 
Cambiado a rama 'tags'
    git cherry-pick nueva-funcionalidad 
[tags 7b63fc2] creo el capitulo 5
 Date: Tue Oct 22 23:11:42 2024 +0100
 2 files changed, 45 insertions(+), 1 deletion(-)
 create mode 100644 capitulos/Capitulo5.txt
 ```
 ### mostrar el historial
 ```code
    git log
commit 7b63fc2dffc882c56c53907dc720e1c90f0b6965 (HEAD -> tags)
Author: alejandrosalazargonzalez <alejandrosalazargonzalez2004@gmail.com>
Date:   Tue Oct 22 23:11:42 2024 +0100

    creo el capitulo 5
```
## Ejercicio 4: Comparar ramas
### modificar el readme y comprobar la diferencia con la rama nueva-funcioanalidad
```code
git diff 7b63fc2dffc882c56c53907dc720e1c90f0b6965..54d66e76f5bce6ac55249030c4aed681fe249a35
diff --git a/README.md b/README.md
index ad9b826..542c290 100644
--- a/README.md
+++ b/README.md
@@ -22,48 +22,5 @@ Cambios no rastreados para el commit:
         modificados:     capitulos/Capitulo1.txt
 
 sin cambios agregados al commit (usa "git add" y/o "git commit -a")
-```
-### Muestra el historial de commits
-```code
-    git log
-commit 54d66e76f5bce6ac55249030c4aed681fe249a35 (HEAD -> tags)
-Author: alejandrosalazargonzalez <alejandrosalazargonzalez2004@gmail.com>
-Date:   Tue Oct 22 23:01:54 2024 +0100
-
-    Revert "Revert "Revert "modifique el readme"""
-    
-    This reverts commit 86bc59cb6129d1d8487787af5ba32b8771ee3eec.
-
-commit 86bc59cb6129d1d8487787af5ba32b8771ee3eec
-Author: alejandrosalazargonzalez <alejandrosalazargonzalez2004@gmail.com>
-Date:   Tue Oct 22 22:57:40 2024 +0100
-
-    Revert "Revert "modifique el readme""
-    
-    This reverts commit b4181b787b61942029e38d03f55b936c2b6ca138.
-
-commit b4181b787b61942029e38d03f55b936c2b6ca138
-Author: alejandrosalazargonzalez <alejandrosalazargonzalez2004@gmail.com>
-Date:   Tue Oct 22 22:55:47 2024 +0100
-
-    Revert "modifique el readme"
-    
-    This reverts commit 5d0e48c15a39c4bf3ebfca1df4224cf9feb1ceb0.
 
-commit 5d0e48c15a39c4bf3ebfca1df4224cf9feb1ceb0 (origin/tags)
-Author: alejandrosalazargonzalez <alejandrosalazargonzalez2004@gmail.com>
-Date:   Tue Oct 22 22:55:14 2024 +0100
-
-    modifique el readme
-
-commit 2c4f64f2940448362f3731c3afb5c0ccb77c4250
-Author: alejandrosalazargonzalez <alejandrosalazargonzalez2004@gmail.com>
-Date:   Tue Oct 22 22:47:55 2024 +0100
-
-    Agregada una linea en Capitulo1.txt
-```
-
-## Ejercicio 3: Aplicar cambios de otra rama con Cherry-pick
-### Crea una nueva rama llamada nueva-funcionalidad y haz un cambio en la rama
-```code
-```
+```
\ No newline at end of file
diff --git a/capitulos/Capitulo5.txt b/capitulos/Capitulo5.txt
deleted file mode 100644
index ce1b8bb..0000000
--- a/capitulos/Capitulo5.txt
+++ /dev/null
@@ -1 +0,0 @@
-En este capítulo veremos cómo gestionar múltiples ramas en Git.
```
## Ejercicio 5: Resolver conflictos de fusión
### merge de los cambios en las ramas
```code 
git merge tags nueva-funcionalidad 
Auto-fusionando README.md
CONFLICTO (contenido): Conflicto de fusión en README.md
Fusión automática falló; arregle los conflictos y luego realice un commit con el resultado.
bae2@jpexposito-VirtualBox:~/Documentos/ejercicio-git-libro$ git status 
En la rama tags
Cambios no rastreados para el commit:
  (usa "git add <archivo>..." para actualizar lo que será confirmado)
  (usa "git restore <archivo>..." para descartar los cambios en el directorio de trabajo)
        modificados:     README.md

sin cambios agregados al commit (usa "git add" y/o "git commit -a")
bae2@jpexposito-VirtualBox:~/Documentos/ejercicio-git-libro$ git add .
bae2@jpexposito-VirtualBox:~/Documentos/ejercicio-git-libro$ git co
commit   config   
bae2@jpexposito-VirtualBox:~/Documentos/ejercicio-git-libro$ git commit -m "merge del readme"
[tags 1643c4f] merge del readme
 1 file changed, 1 insertion(+)
 ```
 ## Ejercicio 6: Revertir un merge
 ### realizo un merge
 ```code 
    git merge tags nueva-funcionalidad 
Auto-fusionando capitulos/Capitulo2.txt
CONFLICTO (contenido): Conflicto de fusión en capitulos/Capitulo2.txt
```
### realizo el git revert
```code
    git revert -m 1 cb3e981
[tags c01aa4b] Revert "merge aa revertir"
 1 file changed, 2 deletions(-)
```
## Ejercicio 7: Eliminar una etiqueta
### Borra la etiqueta v1.0 
```code
    git tag 
1.0.0
1.0.1
    git tag -d 1.0.0
Etiqueta '1.0.0' eliminada (era b32d7b2)
    git push origin :refs/tags/1.0.0
To https://github.com/alejandrosalazargonzalez/ejercicio-git-libro
 - [deleted]         1.0.0
```
## Ejercicio 8: Restablecer un commit (Reset)
```code
    git add .
    git commit -m "Ejercicios hasta el 8"
[tags 97f2c25] Ejercicios hasta el 8
 1 file changed, 24 insertions(+), 1 deletion(-)

    git push origin tags 
Enumerando objetos: 33, listo.
Contando objetos: 100% (32/32), listo.
Compresión delta usando hasta 6 hilos
Comprimiendo objetos: 100% (25/25), listo.
Escribiendo objetos: 100% (25/25), 2.93 KiB | 300.00 KiB/s, listo.
Total 25 (delta 16), reusados 0 (delta 0), pack-reusados 0
remote: Resolving deltas: 100% (16/16), completed with 4 local objects.
To https://github.com/alejandrosalazargonzalez/ejercicio-git-libro
   c658461..97f2c25  tags -> tags

    git reset --hard
HEAD está ahora en 97f2c25 Ejercicios hasta el 8
```
