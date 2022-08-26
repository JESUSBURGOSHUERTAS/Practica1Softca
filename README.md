[![unnamed.png](https://i.postimg.cc/G9wMSWMs/unnamed.png)](https://postimg.cc/Cn7HRQpF)

### Comandos: 💻
##### Crear repositorio

1. Crear un repositorio en vuestro GitHub llamado Practica1Softca
2. Clonar vuestro repositorio en local.

- Primero se clona el repositorio en local:
`git clone git@github.com:JESUSBURGOSHUERTAS/Practica1Softca.git`
- Luego nos ubicamos en la carpeta del proyecto:
`cd Practica1Softca/`
#####3. Crear (si no lo habéis creado ya) en vuestro repositorio local  un documento README.md.

- Creamos el archivo **README.md** con el siguiente comando:
`touch README.md`
##### 4. Añadir al README.md los comandos utilizados hasta ahora y hacer un commit inicial con el mensaje commit inicial.

- Podemos usar vim o el editor preferido para editar el archivo y anexar los comandos:
    ```markdown
vim README.md
git add .
git commit -m "commit inicial"
```
##### 5. Subir los cambios al repositorio remoto.
`git push origin main`
##### Ignorar archivos
6. Crear en el repositorio local un fichero llamado privado.txt.
`touch privado.txt`
7. Crear en el repositorio local una carpeta llamada privada.
`mkdir privada`
8. Realizar los cambios oportunos para que tanto el archivo como la carpeta sea ignorada por git.
```markdown
touch .gitignore
vim .gitignore
```
Añadimos lo siguiente dentro del editor:
```markdown
privado.txt
privada/
```
##### 9. Añadir fichero 1.txt al repositorio local.
` touch 1.txt`
Crear el tag v0.1
` git tag v0.1`

##### Subir el tag v0.1
11.Subir los cambios al repositorio remoto
```markdown
git push --tag origin main
git add .
git commit -m "se añade fichero 1.txt"
```
##### 12. Crear una rama v0.2.
`git branch v0.2`
##### 13. Posiciona tu carpeta de trabajo en esta rama.13. Posiciona tu carpeta de trabajo en esta rama.
`git checkout v0.2`
##### 14. Añadir un fichero 2.txt en la rama v0.2
`touch 2.txt`
##### 15. Subir los cambios al repositorio remoto.15. Subir los cambios al repositorio remoto.
```markdown
git add .
git commit -m "rama 2 se añade"
```
##### 16. Posicionarse en la rama main.
 `git checkout main`
##### 17.Hacer un merge de la rama v0.2 en la rama master.
` git merge v0.2`
#### Merge con conflicto
##### 18. En la rama master poner Hola en el fichero 1.txt y hacer commit.
```markdown
vim 1.txt
git add .
git commit -m "se añade hola en el fichero 1.txt"
```
##### 19. Posicionarse en la rama v0.2 y poner Adios en el fichero "1.txt" y hacer commit.
```markdown
git checkout v0.2
vim 1.txt
git add .
git commit -m "se añade adios en 1.txt"
```
##### 20. Posicionarse de nuevo en la rama master y hacer un merge con la rama v0.2
```markdown
git checkout main
git merge v0.2
```
##### 21. Listar las ramas con merge y las ramas sin merge.
```markdown
git branch --merged
git branch --no-merged
```
##### 22. Arreglar el conflicto anterior y hacer un commit.
```markdown
vim 1.txt
git add .
git commit -m "conflicto solucionado"
```
##### 23. Crear un tag v0.2
`git tag v0.2`
##### 24. Borrar la rama v0.2
`git branch -d v0.2`
##### 25. Listar los distintos commits con sus ramas y sus tags.
```markdown
 alias arbolito="git log --all --graph --decorate --oneline"
arbolito
```
