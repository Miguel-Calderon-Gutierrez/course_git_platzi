# Guía de Git en Español

Esta guía te proporcionará los comandos básicos para comenzar a usar Git en tu proyecto y manejar tu repositorio de manera eficiente.

## Inicialización y Configuración Básica
### 1. Iniciar un repositorio Git:
```bash
 git init
```
### 2.Ver el estado del repositorio:
```bash
git status
```
### 3.Eliminar un archivo del área de preparación (staging area):
```bash
git rm --cached historia.txt
```
### 4.Agregar archivos al área de preparación:
```bash
git add .
```
### 5.Hacer un commit:
`git commit -m "este es el primer commit"`
### 6.Configurar tu nombre de usuario y correo electrónico:
```bash
git config --global user.name "Miguel Calderon"
git config --global user.email "miguelcalderon.dev@gmail.com"
```
### 7.Ver Cambios y Diferencias
#### Ver los cambios de un archivo específico:
```bash
git show historia.txt
```
##### Ver las diferencias entre dos versiones:
```bash
git diff version1 version2
```
## Historial y Versiones

### Obtener el historial de commits:
```bash
git log
```

### Volver a una versión específica:
```bash
git checkout version
```

### Clonar un repositorio:
```bash
git clone https://github.com/usuario/repo.git
```

## Ramas

### Crear una nueva rama:
```bash
git branch cabecera
```

### Cambiar a una rama específica:
```bash
git checkout cabecera
```

### Fusionar ramas (merge):
```bash
git merge rama2
```

## Remotos

### Agregar un origen remoto:
```bash
git remote add origin https://github.com/usuario/repo.git
```

### Enviar cambios al origen remoto:
```bash
git push origin main
```

### Traer cambios del remoto al local:
```bash
git pull origin main
```

### Combinar historias:
```bash
git pull origin main --allow-unrelated-histories
```

## Alias

### Crear un alias para comandos largos:
```bash
alias arbolito="git log --all --graph --decorate --oneline"
arbolito
```

## Tags

### Crear tags para las versiones del código:
```bash
git tag -a v0.1 -m "Primera versión del proyecto" 9550633da410bf2
```

### Subir los tags al repositorio remoto:
```bash
git push origin --tags
```

### Eliminar tags no necesarios:
```bash
git tag -d TagQueQuieroBorrar
git push origin --tags
git push origin :refs/tags/TagQueQuieroBorrar
```

## Ver Ramas

### Ver todas las ramas:
```bash
git branch
```

### Ver todas las ramas históricamente:
```bash
git show-branch --all
```

### Ver de forma visual:
```bash
gitk
```

### Enviar ramas al remoto:
```bash
git push origin rama2
```

## Nuevas Ramas

### Crear nuevas ramas desde la rama con la versión más reciente:
```bash
git checkout main
git branch header
git branch footer
```

## Otros

### Traer cambios de un proyecto opensource al que le hiciste fork:
```bash
git remote add upstream https://github.com/otrosUsuario/repoAlQueHiceFork.git
git pull upstream main
git commit -am "fusión"
git push origin master
```

### Rebase:
```bash
git rebase main
git rebase experimento
```

### Cambios Temporales:
```bash
git stash
git stash pop
git stash branch nuevaRama
git stash drop
```

### Limpiar el proyecto:
```bash
git clean --dry-run
git clean -f
```

### Traer commits antiguos:
```bash
git cherry-pick dca2a24
```

### Volver a una versión anterior:
```bash
git reflog
git reset --HARD c944564645
```

### Agregar cambios a un commit anterior:
```bash
git commit --amend
```

### Buscar palabras en el repositorio:
```bash
git grep palabraABuscar
git grep -c lapalabraquequierocontar
```

### Buscar en el historial de commits:
```bash
git log -s "palabra"
```

## Alias Internos en Git

### Mostrar cuántos commits han hecho cada miembro del equipo:
```bash
git shortlog -sn
```

### Mostrar cuántos commits han hecho cada miembro del equipo (incluyendo los eliminados):
```bash
git shortlog -sn --all
```

### Mostrar cuántos commits han hecho cada miembro (sin los merges):
```bash
git shortlog -sn --all --no-merge
```

### Mostrar quién hizo cada línea de un archivo:
```bash
git blame ARCHIVO
```

### Mostrar quién hizo cada línea de un archivo en un rango específico:
```bash
git blame ARCHIVO -L35,50
```

### Ver todas las ramas remotas:
```bash
git branch -r
```

### Ver todas las ramas locales y remotas:
```bash
git branch -a
```

### Crear un alias:
```bash
git config --global alias.nombreDelAlias "comando de git que quiero asignarle al alias"
```

### Mostrar ayuda de un comando:
```bash
git COMANDO --help
```

