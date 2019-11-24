1.¿Qué comando utilizaste en el paso 11? ¿Por qué?
git reset --hard HEAD~1
Para deshacer un commit podemos utilizar el comando git reset y al querer perder los cambios realizados en el working copy utilizamos el atributo --hard, HEAD-1 indica que queremos retroceder un paso para atrás en este caso el commit anterior.

2.¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?
Primero hice un git reflog para ver el id del estado al que quiero volver, luego con el comando git reset --hard id volví al commit anterior y recuperé los datos de ese commit, por otro lado probé a hacerlo con git checkout idCommit, tras un reset anterior, y también recupera el commit, vuelves a él, pero no esta en ninguna rama entras en el estado 'detached HEAD' al parecer es un estado experimental para hacer pruebas, para crear la rama sería con git checkout -b nombreNuevaRama, en mi opinión el primer paso utilizado es mucho más eficiente.

3.El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
Ubicado en la rama styled y haciendo un git merge master, la rama styled absorbe a master sin ningún conflicto, mensaje de respuesta Ya está actualizado.

4.El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
Sí, debido a que el contenido de los archivos git-nuestro.md es distinto en la rama htmlify y styled, por lo cual habría que indicarle con que archivo nos queremos quedar de ambas ramas aplicando cambios sobre ellos.

5.El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
No ha causado ningun conflicto, lo que ha ocurrido esque la rama master ha absorbido a la rama styled mediante un merge fast-forward actualizando el contenido de master al de styled

6.¿Qué comando o comandos utilizaste en el paso 25?
git log --graph

7.El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?
Sí ya que no hace falta crear un nuevo commit para que master absorba a Title, en este caso master únicamente tiene que desplazar su puntero hasta el commit de la rama Title para absorber sus características.

8.¿Qué comando o comandos utilizaste en el paso 27?
git reset c3e42d756d6bd3d837ac7d7d408d100578a1d22c indicando el commit al que queremos volver en este caso el commit antes de realizar el merge con la rama title, al no querer perder los cambios del working copy no utilizamos el atributo --hard

9.¿Qué comando o comandos utilizaste en el paso 28?
git reset HEAD@{3}, con este  comando gracias a la selección directa retrocedemos al estado donde el git-nuestro.md no tenía título todavía y así descartamos los cambios

10.¿Qué comando o comandos utilizaste en el paso 29?
git branch -d title

11.¿Qué comando o comandos utilizaste en el paso 30?
Primero el comando git reflog para ver en que estado habíamos realizado el merge, una vez lo localizamos utilizo el comando git reset HEAD@{4} para rehacer el merge.

12.¿Qué comando o comandos usaste en el paso 32?
Primero el comando git log para ver el idHash del primer commit, una vez lo localizamos utilizo el comando git reset 6eaa597d3ba934bfce5adbc1aa9a7efe9a971681 para volver a ese commit, en este caso el primero.

13.¿Qué comando o comandos usaste en el punto 33?
git reflog para localizar donde pusimos título al poema, una vez localizado con el comando git reset HEAD@{9} para llegar a ese estado y comprobar que esta el título.

