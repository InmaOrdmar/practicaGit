# Preguntas de la práctica

## ¿Qué comando utilizaste en el paso 11? ¿Por qué?

He utilizado `git reset --hard HEAD~1`. El `reset HEAD~1` me permite volver al commit padre llevándome conmigo también la rama styled hacia abajo, si añado `--hard` además los cambios desaparecen del working copy y el staging area queda vacío.

## ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?

Primero he utilizado `git reflog` para localizar el identificador del commit que acabamos de deshacer. Lo he copiado y posteriormente he utilizado el comando `git reset --hard <identificador>`. Este comando me permite volver al commit que habíamos deshecho y al incluir `--hard`, los cambios se ven reflejados en el working copy.

## El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?

No, porque realmente no hay ningún cambio. La rama styled ya contiene todos los commits que forman parte de master (que en este caso es solamente el inicial). Por esta razón, git muestra el mensaje "Already up to date".

## El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?

Sí, porque hay una o más líneas del archivo git-nuestro.md que son diferentes entre las dos ramas (en este caso, todas las líneas son diferentes pero bastaría con que una fuera diferente para generar conflicto). Para evitar perder trabajo realizado, git crea el conflicto y nos pide que lo solucionemos, guardando la versión que prefiramos del archivo y haciendo commit de esta versión antes de cerrar el merge.

## El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?

No, porque ha sido un merge fast-forward en el que no se ha creado ningún commit nuevo, la rama master simplemente se situa en el último commit de styled y por tanto gana acceso a todos los commits de esa rama.

## ¿Qué comando o comandos utilizaste en el paso 25?

`git log --graph --decorate --pretty=oneline`

## El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?

Sí, podría serlo porque al estar las dos ramas en línea no sería necesario hacer un nuevo commit para realizar el merge.

## ¿Qué comando o comandos utilizaste en el paso 27? 

`git reset HEAD~1`

## ¿Qué comando o comandos utilizaste en el paso 28?

`git checkout -- git-nuestro.md`

## ¿Qué comando o comandos utilizaste en el paso 29?

`git branch -D title`

## ¿Qué comando o comandos utilizaste en el paso 30?

`git reflog` para encontrar la referencia del commit en el que estábamos justo después de hacer el merge
`git reset --hard <identificador>` para rehacer el commit

## ¿Qué comando o comandos usaste en el paso 32?

`git checkout <identificador>` (utilizo el primer identificador de la lista obtenida con el reflog del paso 30)

## ¿Qué comando o comandos usaste en el punto 33?

`git checkout master`
