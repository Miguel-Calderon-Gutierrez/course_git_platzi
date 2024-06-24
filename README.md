# Guía de Git en Español

Esta guía te proporcionará los comandos básicos para comenzar a usar Git en tu proyecto y manejar tu repositorio de manera eficiente.

## Inicialización y Configuración Básica
### 1. Iniciar un repositorio Git:
`    git init`
### 2.Ver el estado del repositorio:
`git status`
### 3.Eliminar un archivo del área de preparación (staging area):
`git rm --cached historia.txt`
### 4.Agregar archivos al área de preparación:
`git add .`
### 5.Hacer un commit:
`git commit -m "este es el primer commit"`
### 6.Configurar tu nombre de usuario y correo electrónico:
`git config --global user.name "Miguel Calderon"`
`git config --global user.email "miguelcalderon.dev@gmail.com"`
### 7.Ver Cambios y Diferencias
#### Ver los cambios de un archivo específico:
`git show historia.txt`
##### Ver las diferencias entre dos versiones:
`git diff version1 version2`

Ver el historial de commits:

bash
Copiar código
git log
Volver a una versión específica:

bash
Copiar código
git checkout version
Clonar y Fusionar
Clonar un repositorio remoto:

bash
Copiar código
git clone <url-del-repositorio>
Crear y cambiar a una nueva rama:

bash
Copiar código
git branch cabecera
git checkout cabecera
Fusionar una rama a la rama principal (main):

bash
Copiar código
git checkout main
git merge rama2
Trabajo con Repositorios Remotos
Agregar un origen remoto:

bash
Copiar código
git remote add origin https://github.com/...
Enviar cambios al origen remoto:

bash
Copiar código
git push origin main
Actualizar el repositorio local con cambios del remoto:

bash
Copiar código
git pull origin main
Combinar historias no relacionadas:

bash
Copiar código
git pull origin main --allow-unrelated-histories
Alias y Etiquetas
Crear un alias para comandos largos:

bash
Copiar código
alias arbolito="git log --all --graph --decorate --oneline"
arbolito
Crear etiquetas para versiones del código:

bash
Copiar código
git tag -a v0.1 -m "primera versión del proyecto" 093cc72
Subir etiquetas al repositorio remoto:

bash
Copiar código
git push origin --tags
Eliminar etiquetas innecesarias:

bash
Copiar código
git tag -d TagQueQuieroBorrar
git push origin --tags
git push origin :ref/tags/TagQueQuieroBorrar
Manejo de Ramas
Ver todas las ramas:

bash
Copiar código
git branch
Ver todas las ramas históricamente:

bash
Copiar código
git show-branch --all
Ver las ramas de forma visual:

bash
Copiar código
gitk
Enviar ramas al remoto:

bash
Copiar código
git checkout rama2
git push origin rama2
Crear nuevas ramas desde la versión más reciente:

bash
Copiar código
git checkout main
git branch header
git branch footer
Colaboración y Actualización de Forks
Hacer un merge con la rama de un extraño mediante un pull request en GitHub, revisado por un líder de equipo.

Traer cambios de un proyecto open-source al que hiciste fork:

bash
Copiar código
git remote add upstream https://github.com/otroUsuario/repoAlQueHiceFork
git pull upstream main
git commit -am "fusión"
git push origin master
Esta guía proporciona una visión general de los comandos básicos y algunos avanzados de Git. Úsala como referencia rápida para manejar tus repositorios de manera eficiente