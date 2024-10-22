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

    git add .

    git commit -m "Agregada una linea en Capitulo1.txt"
[tags 2c4f64f] Agregada una linea en Capitulo1.txt
 2 files changed, 26 insertions(+), 715 deletions(-)
 rewrite README.md (98%)
```