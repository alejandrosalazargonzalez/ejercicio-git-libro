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
```
