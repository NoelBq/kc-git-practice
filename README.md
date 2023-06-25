# Practica git - KC mobile

### - Paso 11 

```
git reset --hard HEAD~
```

use este comando elimina el último commit y descarta por completo los cambios realizados en ese commit.

### - Paso 12 

```
git reflog
git reset <identificador_del_commit>
```

`git reflog` para checkear el identificador del commit y luego `git reset` seguido del identificador del commit para deshacer el reset y regresar al estado anterior:

### - Paso 13

si hay conflictos, ya que styled al absorver a main trae el archivo antes de los cambios(agregar asterioscos) donde partio styled, hay que resolver conflictos para hacer el merge, intuyo que quedandose con los cambios de main

## - Paso 21

no genera conflictos porque previamente en el paso 13 hicimos un merge con master, osea que styled absorvio a main, resolviendo los conflictos quedandose con el contenido de master, por lo tanto en el momento que se hizo el merge de htmlify y se sostuvieron los cambios de styled, styled y master estaban en iguales condiciones.

### - Paso 19

hay conflictos porque la rama `htmlify` tiene `<em>` tags y la rama styled no, se conserva los current de la rama `styled` para resolver conflictos, de acuerdo al enunciado

### - Paso 25

```
git log --graph --oneline --decorate --all
```

`--graph`: muestra el grafo de commits.
`--oneline`: muestra cada commit en una sola línea
`--decorate`: Muestra las referencias (ramas, etiquetas)
`--all`: muestra todos los commits de todas las ramas.

### - Paso 26

El merge puede ser ff porque se puede hacer ocurre cuando una rama esta por delante de la otra, no hay cambios en la rama que recibe el merge, en este caso main. En el merge -ff no se crea un nuevo commit

### - Paso 27

```
git reflog
git revert <identificador_del_commit>
```

`git reflog` para checkear el identificador del commit y luego `git revert` seguido del identificador del commit para ir al commit antes del merge, Se usa `git revert` para mantener los cambios del working copy

### - Paso 28

```
git reset HEAD~
```

para descartar cambios de working copy

### - Paso 29

```
git branch -d title
```

en este caso se puede usar -d miniscula porque main tiene esta rama ya fusionada.

### - Paso 30

```
git reflog
git merge  <identificador_del_commit>
```

buscamos el identificador del commit del merge con reflog, que al haber sido un merge no-ff crea un commit al hacer el merge y luego ponemos el identificador del mismo

## - Paso 32

```
git reflog
git reset --hard <identificador_del_commit>
```

hacemos un hard reset al punto donde hicimos el primer commit con la creacion del poema, si queremos dejar el working copy como estaba en el momento de ese commit 

## - Paso 33

```
git reflog
git reset --hard <identificador_del_commit_merge_title>
```

en este caso iria al commit donde se mergeo la rama title donde se creo el titulo.
