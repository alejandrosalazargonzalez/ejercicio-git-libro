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

    git add .

    git commit -m "Añadido capítulo 2  y actualización del README."
[main 7c68b25] Añadido capítulo 2  y actualización del README.
 2 files changed, 31 insertions(+), 1 deletion(-)
 create mode 100644 capitulos/Capitulo2.txt
```
### Compruebo las diferencias de esta versión con las 2 anteriores 
````code
    git diff HEAD~2..HEAD 
diff --git a/README.md b/README.md
index 6fd3fb7..c38a14b 100644
--- a/README.md
+++ b/README.md
@@ -76,4 +76,35 @@ Date:   Thu Oct 10 18:01:20 2024 +0100
 ```
 
 ## Ejercicio 2
-### Creo el Capitulo3.txt
\ No newline at end of file
+### Creo el Capitulo2.txt
+```code
+El flujo de trabajo básico con Git consiste en:
+ 1- Hacer cambios en el repositorio.
+ 2- Añadir los cambios a la zona de intercambio temporal.
+ 3- Hacer un commit de los cambios.
+```
+### Subir los cambios a la zona de intercambio
+```code
+    git status 
+En la rama main
+Tu rama está adelantada a 'origin/main' por 2 commits.
+  (usa "git push" para publicar tus commits locales)
+
+Cambios no rastreados para el commit:
+  (usa "git add <archivo>..." para actualizar lo que será confirmado)
+  (usa "git restore <archivo>..." para descartar los cambios en el directorio de trabajo)
+        modificados:     README.md
+
+Archivos sin seguimiento:
+  (usa "git add <archivo>..." para incluirlo a lo que será confirmado)
+        capitulos/Capitulo2.txt
+
+sin cambios agregados al commit (usa "git add" y/o "git commit -a")
+
+    git add .
+
+    git commit -m "Añadido capítulo 2  y actualización del README."
+[main 7c68b25] Añadido capítulo 2  y actualización del README.
+ 2 files changed, 31 insertions(+), 1 deletion(-)
+ create mode 100644 capitulos/Capitulo2.txt
+```
diff --git a/capitulos/Capitulo2.txt b/capitulos/Capitulo2.txt
new file mode 100644
index 0000000..e2034e0
--- /dev/null
+++ b/capitulos/Capitulo2.txt
@@ -0,0 +1,4 @@
+El flujo de trabajo básico con Git consiste en:
+ 1- Hacer cambios en el repositorio.
+ 2- Añadir los cambios a la zona de intercambio temporal.
+ 3- Hacer un commit de los cambios.
\ No newline at end of file
(END)
````
## Ejercicio 3
### Creo el capitulo 3
```code
Git permite la creación de ramas lo que permite tener distintas versiones del mismo proyecto y trabajar de manera simultanea en ellas.
```
### Añado los cambios a la zona temporal
```code
    git status
En la rama main
Tu rama está adelantada a 'origin/main' por 4 commits.
  (usa "git push" para publicar tus commits locales)

Cambios no rastreados para el commit:
  (usa "git add <archivo>..." para actualizar lo que será confirmado)
  (usa "git restore <archivo>..." para descartar los cambios en el directorio de trabajo)
        modificados:     README.md

Archivos sin seguimiento:
  (usa "git add <archivo>..." para incluirlo a lo que será confirmado)
        capitulos/Capitulo3.txt

sin cambios agregados al commit (usa "git add" y/o "git commit -a")ç

    git add .

    git commit -m "Añadido capitulo 3 y cambios al README"
[main af2c8e6] Añadido capitulo 3 y cambios al README
 2 files changed, 84 insertions(+)
 create mode 100644 capitulos/Capitulo3.txt
```
### ejecuto el git log y el git diff
````code
    git log
commit c01d770a666b1016fc785ed630840eb8a02e97ba (HEAD -> main)
Author: alejandrosalazargonzalez <alejandrosalazargonzalez2004@gmail.com>
Date:   Thu Oct 10 18:35:49 2024 +0100

    Actualizacion del README

commit af2c8e6ec360c470c43c1d65a36b3ab603ee33fc
Author: alejandrosalazargonzalez <alejandrosalazargonzalez2004@gmail.com>
Date:   Thu Oct 10 18:34:19 2024 +0100

    Añadido capitulo 3 y cambios al README

commit 51c427a85970b28890f8b32ab895a7373410f679
Author: alejandrosalazargonzalez <alejandrosalazargonzalez2004@gmail.com>
Date:   Thu Oct 10 18:24:42 2024 +0100

    añado el paso anterior al informe del README

commit 7c68b253fe19db261be1adecafdb24429a3eb9d7
Author: alejandrosalazargonzalez <alejandrosalazargonzalez2004@gmail.com>
Date:   Thu Oct 10 18:23:30 2024 +0100

    Añadido capítulo 2  y actualización del README.

commit 8e51745f48fc597369e9b5fd975b6480eda91c12
Author: alejandrosalazargonzalez <alejandrosalazargonzalez2004@gmail.com>
Date:   Thu Oct 10 18:19:20 2024 +0100

    actualizacion del README

commit 8331191c34c867db20edbca2d6051b36aa5c1368
Author: alejandrosalazargonzalez <alejandrosalazargonzalez2004@gmail.com>
Date:   Thu Oct 10 18:13:38 2024 +0100

    Añadido capitulo 1

commit 6b20ec1667976c5a0897caeb91f84b60b49734f8 (origin/main, origin/HEAD)
Author: Salazar <115075962+alejandrosalazargonzalez@users.noreply.github.com>
Date:   Thu Oct 10 18:01:20 2024 +0100

    Initial commit
(END)
````
---
---
````code
    git diff 6b20ec1667976c5a0897caeb91f84b60b49734f8..HEAD
diff --git a/README.md b/README.md
index 9a06b52..82683d2 100644
--- a/README.md
+++ b/README.md
@@ -1 +1,199 @@
-# ejercicio-git-libro
\ No newline at end of file
+# ejercicio-git-libro
+
+## Clono el repositorio
+```code
+    git clone https://github.com/alejandrosalazargonzalez/ejercicio-git-libro.git
+Clonando en 'ejercicio-git-libro'...
+remote: Enumerating objects: 3, done.
+remote: Counting objects: 100% (3/3), done.
+remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
+Recibiendo objetos: 100% (3/3), listo.
+
+    ls -la
+total 16
+drwxrwxr-x 3 bae2 bae2 4096 oct 10 18:01 .
+drwxr-xr-x 7 bae2 bae2 4096 oct 10 18:01 ..
+drwxrwxr-x 8 bae2 bae2 4096 oct 10 18:01 .git
+-rw-rw-r-- 1 bae2 bae2   21 oct 10 18:01 README.md
+```
+## Ejercicio 1
+### Ejecuto el comando log
+```code
+    git log
+commit 6b20ec1667976c5a0897caeb91f84b60b49734f8 (HEAD -> main, origin/main, origin/HEAD)
+Author: Salazar <115075962+alejandrosalazargonzalez@users.noreply.github.com>
+Date:   Thu Oct 10 18:01:20 2024 +0100
+
+    Initial commit
+```
+### Creo la carpeta capitulos y el archivo "capitulo1.txt"
+```code
+    mkdir capitulos
+
+    Git es un sistema de control de versiones ideado por Linus Torvalds.
+```
+
+### Añado los cambios a la zona de intercambios
+```code
+    git status 
+En la rama main
+Tu rama está actualizada con 'origin/main'.
+
+Cambios no rastreados para el commit:
+  (usa "git add <archivo>..." para actualizar lo que será confirmado)
+  (usa "git restore <archivo>..." para descartar los cambios en el directorio de trabajo)
+        modificados:     README.md
+
+Archivos sin seguimiento:
+  (usa "git add <archivo>..." para incluirlo a lo que será confirmado)
+        capitulos/
+
+sin cambios agregados al commit (usa "git add" y/o "git commit -a")
+
+    git add .
+
+    git commit -m "Añadido capitulo 1"
+[main 8331191] Añadido capitulo 1
+ 2 files changed, 35 insertions(+), 1 deletion(-)
+ rewrite README.md (100%)
+ create mode 100644 capitulos/Capitulo1.txt
+```
+
+### ejecuto de nuevo el comando git log
+```code
+git log
+commit 8331191c34c867db20edbca2d6051b36aa5c1368 (HEAD -> main)
+Author: alejandrosalazargonzalez <alejandrosalazargonzalez2004@gmail.com>
+Date:   Thu Oct 10 18:13:38 2024 +0100
+
+    Añadido capitulo 1
+
+commit 6b20ec1667976c5a0897caeb91f84b60b49734f8 (origin/main, origin/HEAD)
+Author: Salazar <115075962+alejandrosalazargonzalez@users.noreply.github.com>
+Date:   Thu Oct 10 18:01:20 2024 +0100
+
+    Initial commit
+```
+
+## Ejercicio 2
+### Creo el Capitulo2.txt
+```code
+El flujo de trabajo básico con Git consiste en:
+ 1- Hacer cambios en el repositorio.
+ 2- Añadir los cambios a la zona de intercambio temporal.
+ 3- Hacer un commit de los cambios.
+```
+### Subir los cambios a la zona de intercambio
+```code
+    git status 
+En la rama main
+Tu rama está adelantada a 'origin/main' por 2 commits.
+  (usa "git push" para publicar tus commits locales)
+
+Cambios no rastreados para el commit:
+  (usa "git add <archivo>..." para actualizar lo que será confirmado)
+  (usa "git restore <archivo>..." para descartar los cambios en el directorio de trabajo)
+        modificados:     README.md
+
+Archivos sin seguimiento:
+  (usa "git add <archivo>..." para incluirlo a lo que será confirmado)
+        capitulos/Capitulo2.txt
+
+sin cambios agregados al commit (usa "git add" y/o "git commit -a")
+
+    git add .
+
+    git commit -m "Añadido capítulo 2  y actualización del README."
+[main 7c68b25] Añadido capítulo 2  y actualización del README.
+ 2 files changed, 31 insertions(+), 1 deletion(-)
+ create mode 100644 capitulos/Capitulo2.txt
+```
+### Compruebo las diferencias de esta versión con las 2 anteriores 
+````code
+    git diff HEAD~2..HEAD 
+diff --git a/README.md b/README.md
+index 6fd3fb7..c38a14b 100644
+--- a/README.md
++++ b/README.md
+@@ -76,4 +76,35 @@ Date:   Thu Oct 10 18:01:20 2024 +0100
+ ```
+ 
+ ## Ejercicio 2
+-### Creo el Capitulo3.txt
+\ No newline at end of file
++### Creo el Capitulo2.txt
++```code
++El flujo de trabajo básico con Git consiste en:
++ 1- Hacer cambios en el repositorio.
++ 2- Añadir los cambios a la zona de intercambio temporal.
++ 3- Hacer un commit de los cambios.
++```
++### Subir los cambios a la zona de intercambio
++```code
++    git status 
++En la rama main
++Tu rama está adelantada a 'origin/main' por 2 commits.
++  (usa "git push" para publicar tus commits locales)
++
++Cambios no rastreados para el commit:
++  (usa "git add <archivo>..." para actualizar lo que será confirmado)
++  (usa "git restore <archivo>..." para descartar los cambios en el directorio de trabajo)
++        modificados:     README.md
++
++Archivos sin seguimiento:
++  (usa "git add <archivo>..." para incluirlo a lo que será confirmado)
++        capitulos/Capitulo2.txt
++
++sin cambios agregados al commit (usa "git add" y/o "git commit -a")
++
++    git add .
++
++    git commit -m "Añadido capítulo 2  y actualización del README."
++[main 7c68b25] Añadido capítulo 2  y actualización del README.
++ 2 files changed, 31 insertions(+), 1 deletion(-)
++ create mode 100644 capitulos/Capitulo2.txt
++```
+diff --git a/capitulos/Capitulo2.txt b/capitulos/Capitulo2.txt
+new file mode 100644
+index 0000000..e2034e0
+--- /dev/null
++++ b/capitulos/Capitulo2.txt
+@@ -0,0 +1,4 @@
++El flujo de trabajo básico con Git consiste en:
++ 1- Hacer cambios en el repositorio.
++ 2- Añadir los cambios a la zona de intercambio temporal.
++ 3- Hacer un commit de los cambios.
+\ No newline at end of file
+(END)
+````
+## Ejercicio 3
+### Creo el capitulo 3
+```code
+Git permite la creación de ramas lo que permite tener distintas versiones del mismo proyecto y trabajar de manera simultanea en ellas.
+```
+### Añado los cambios a la zona temporal
+```code
+    git status
+En la rama main
+Tu rama está adelantada a 'origin/main' por 4 commits.
+  (usa "git push" para publicar tus commits locales)
+
+Cambios no rastreados para el commit:
+  (usa "git add <archivo>..." para actualizar lo que será confirmado)
+  (usa "git restore <archivo>..." para descartar los cambios en el directorio de trabajo)
+        modificados:     README.md
+
+Archivos sin seguimiento:
+  (usa "git add <archivo>..." para incluirlo a lo que será confirmado)
+        capitulos/Capitulo3.txt
+
+sin cambios agregados al commit (usa "git add" y/o "git commit -a")ç
+
+    git add .
+
+    git commit -m "Añadido capitulo 3 y cambios al README"
+[main af2c8e6] Añadido capitulo 3 y cambios al README
+ 2 files changed, 84 insertions(+)
+ create mode 100644 capitulos/Capitulo3.txt
+```
+
diff --git a/capitulos/Capitulo1.txt b/capitulos/Capitulo1.txt
new file mode 100644
index 0000000..f4068a7
--- /dev/null
+++ b/capitulos/Capitulo1.txt
@@ -0,0 +1 @@
+Git es un sistema de control de versiones ideado por Linus Torvalds.
\ No newline at end of file
diff --git a/capitulos/Capitulo2.txt b/capitulos/Capitulo2.txt
new file mode 100644
index 0000000..e2034e0
--- /dev/null
+++ b/capitulos/Capitulo2.txt
@@ -0,0 +1,4 @@
+El flujo de trabajo básico con Git consiste en:
+ 1- Hacer cambios en el repositorio.
+ 2- Añadir los cambios a la zona de intercambio temporal.
+ 3- Hacer un commit de los cambios.
\ No newline at end of file
diff --git a/capitulos/Capitulo3.txt b/capitulos/Capitulo3.txt
new file mode 100644
index 0000000..534b9a9
--- /dev/null
+++ b/capitulos/Capitulo3.txt
@@ -0,0 +1 @@
+Git permite la creación de ramas lo que permite tener distintas versiones del mismo proyecto y trabajar de manera simultanea en ellas.
\ No newline at end of file
(END)
````
## Ejercicio 4
### Creo el indice 
```code
Indice de los cápitulos, con conceptos avanzados de git
```
### Añadir los cambios a la zona de intercambio temporal.
```code
 git add .
 git commit -m "Indice de los cápitulos, con conceptos avanzados de git"
```
### Mostrar quién ha hecho cambios sobre el fichero indice.txt.
```code
    git annotate capitulos/Indice.txt
a7c792b3        (alejandrosalazargonzalez       2024-10-14 15:37:31 +0100       1)Indice de los cápitulos, con conceptos avanzados de git
```
## Ejercicio 5
###  Creo la rama bibliotea y muestro las ramas del repositorio
```code
    git branch bibliografia
    git branch -av
warning: ignorando referencia rota refs/remotes/origin/main
  bibliografia ee78854 se acaba el ejercicio 4
* main         ee78854 [desaparecido] se acaba el ejercicio 4
```
## Ejercicio 6
### Creo el archivo capitulo4.txt
```code
  En este capítulo veremos cómo usar GitHub para alojar repositorios en remoto.
```
### Añado los cambios al espacio de intercambio
```code
    git add .
    git commit -m "Añado el capitulo 4"
[main 85be25d] Añado el capitulo 4
 2 files changed, 7 insertions(+), 1 deletion(-)
 create mode 100644 capitulos/Capitulo4.txt
```
### Ejecuto el comando git log --graph --all --oneline
```code
    git log --graph --all --oneline
* 85be25d (HEAD -> main, origin/main) Añado el capitulo 4
* 684e1f8 ultimo cambio de clase
* ee78854 (bibliografia) se acaba el ejercicio 4
* a7c792b Indice de los cápitulos, con conceptos avanzados de git
* 22c7aa8 Ultimo commit antes de acabar la clase 10/10/2024
* c01d770 Actualizacion del README
* af2c8e6 Añadido capitulo 3 y cambios al README
* 51c427a añado el paso anterior al informe del README
* 7c68b25 Añadido capítulo 2  y actualización del README.
* 8e51745 actualizacion del README
* 8331191 Añadido capitulo 1
* 6b20ec1 Initial commit
```
## Ejercicio 7
### Cambiar a la rama bibliografía
```code 
    git checkout bibliografia 
Cambiado a rama 'bibliografia'
```
### Crear el fichero bibliografia.txt
```code
Chacon, S. and Straub, B. Pro Git. Apress.
```
### Añadir cambios a la zona de intercambio temporal
```code
    git add .
    git commit -m "Añadida la primera referencia bibliografica"
[bibliografia 3158de9] Añadida la primera referencia bibliografica
 1 file changed, 1 insertion(+)
 create mode 100644 bibliografia.txt
```
### Mostrar historial del repositorio incluyendo ramas
```code
    git log --graph --all --oneline
* 3158de9 (HEAD -> bibliografia) Añadida la primera referencia bibliografica
| * a37524d (main) cambios antes de cambiar de rama
| * 85be25d (origin/main) Añado el capitulo 4
| * 684e1f8 ultimo cambio de clase
|/  
* ee78854 se acaba el ejercicio 4
* a7c792b Indice de los cápitulos, con conceptos avanzados de git
* 22c7aa8 Ultimo commit antes de acabar la clase 10/10/2024
* c01d770 Actualizacion del README
* af2c8e6 Añadido capitulo 3 y cambios al README
* 51c427a añado el paso anterior al informe del README
* 7c68b25 Añadido capítulo 2  y actualización del README.
* 8e51745 actualizacion del README
* 8331191 Añadido capitulo 1
* 6b20ec1 Initial commit
```
## Ejercicio 8
### Fusionar la rama bibliografía con la rama main.
```code 
    git checkout main 
Cambiado a rama 'main'
    git merge bibliografia 
Merge made by the 'ort' strategy.
 bibliografia.txt | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 bibliografia.txt
```
### Mostrar la historia del repositorio incluyendo todas las ramas
```code
git log --graph --all --oneline
*   9c01eea (HEAD -> main) Merge branch 'bibliografia'
|\  
| * 3158de9 (bibliografia) Añadida la primera referencia bibliografica
* | a37524d cambios antes de cambiar de rama
* | 85be25d (origin/main) Añado el capitulo 4
* | 684e1f8 ultimo cambio de clase
|/  
* ee78854 se acaba el ejercicio 4
* a7c792b Indice de los cápitulos, con conceptos avanzados de git
* 22c7aa8 Ultimo commit antes de acabar la clase 10/10/2024
* c01d770 Actualizacion del README
* af2c8e6 Añadido capitulo 3 y cambios al README
* 51c427a añado el paso anterior al informe del README
* 7c68b25 Añadido capítulo 2  y actualización del README.
* 8e51745 actualizacion del README
* 8331191 Añadido capitulo 1
* 6b20ec1 Initial commit
```
### Elimino la rama bibliografia
```code
    git branch -d bibliografia
Eliminada la rama bibliografia (era 3158de9).
```
### Muestro el historial del repositorio incluyendo ramas
```code
git log --graph --all --oneline
*   9c01eea (HEAD -> main) Merge branch 'bibliografia'
|\  
| * 3158de9 Añadida la primera referencia bibliografica
* | a37524d cambios antes de cambiar de rama
* | 85be25d (origin/main) Añado el capitulo 4
* | 684e1f8 ultimo cambio de clase
|/  
* ee78854 se acaba el ejercicio 4
* a7c792b Indice de los cápitulos, con conceptos avanzados de git
* 22c7aa8 Ultimo commit antes de acabar la clase 10/10/2024
* c01d770 Actualizacion del README
* af2c8e6 Añadido capitulo 3 y cambios al README
* 51c427a añado el paso anterior al informe del README
* 7c68b25 Añadido capítulo 2  y actualización del README.
* 8e51745 actualizacion del README
* 8331191 Añadido capitulo 1
* 6b20ec1 Initial commit
```
## Ejercicio 9
### Crear la rama bibliografía.
```code
git branch bibliografia
```
### Cambiar a la rama bibliografia
```code
    git checkout bibliografia 
Cambiado a rama 'bibliografia'
```
### Agregar datos al fichero bibliografia
```code
Ryan Hodson. Ry’s Git Tutorial. Smashwords (2014)
```
### hago un commit 
```code
    git commit -m "se ha cambiado el fichero bibliografia.txt"
[bibliografia 309a625] se ha cambiado el fichero bibliografia.txt
```
### Cambiar a la rama main
```code
    git checkout main 
M       bibliografia.txt
Cambiado a rama 'main'
```
### Cambiar fichero bibliografia
```code
Loeliger, J. and McCullough, M. Version control with Git. O’Reilly.
```
### Subo los cambios a la zona de intercambio temporal
```code
    git add .
    git commit -m "Añadida nueva referencia bibliográfica"
[main a9b78ee] Añadida nueva referencia bibliográfica
 1 file changed, 1 insertion(+), 1 deletion(-)
```
### Uno las dos ramas
```code 
    qit merge bibliografia
Auto-fusionando bibliografia.txt
CONFLICTO (contenido): Conflicto de fusión en bibliografia.txt
Fusión automática falló; arregle los conflictos y luego realice un commit con el resultado.
```
### Arreglo lo que me pide
```code
nano bibliografia.txt 
```

### Hago el ultimo commit y muestro el ultimo historial
```code
git commit -a -m "Solucionado conflicto bibliografía."
 git log --graph --all --oneline
[main 68ed887] Solucionado conflicto bibliografía.
*   68ed887 (HEAD -> main) Solucionado conflicto bibliografía.
|\  
| * 9f4148f (bibliografia) Añadida nueva referencia bibliográfica.
* | 6a19808 Añadida nueva referencia bibliográfica.
|/  
*   3a3789c (origin/main, origin/HEAD) commit antes del cambio
|\  
| * 309a625 se ha cambiado el fichero bibliografia.txt
* | a9b78ee Añadida nueva referencia bibliográfica
* | a0299bc cambios antes de cambiar de rama
* | dc059c8 Commit antes de cambiar a la nueva rama bibliografia
|/  
*   9c01eea Merge branch 'bibliografia'
|\  
| * 3158de9 Añadida la primera referencia bibliografica
* | a37524d cambios antes de cambiar de rama
* | 85be25d Añado el capitulo 4
* | 684e1f8 ultimo cambio de clase
|/  
* ee78854 se acaba el ejercicio 4
* a7c792b Indice de los cápitulos, con conceptos avanzados de git
* 22c7aa8 Ultimo commit antes de acabar la clase 10/10/2024
* c01d770 Actualizacion del README
* af2c8e6 Añadido capitulo 3 y cambios al README
* 51c427a añado el paso anterior al informe del README
* 7c68b25 Añadido capítulo 2  y actualización del README.
* 8e51745 actualizacion del README
* 8331191 Añadido capitulo 1
* 6b20ec1 Initial commit
```