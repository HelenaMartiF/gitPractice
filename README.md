# Llorasión

- ¿Qué comando utilizaste en el paso 11? ¿Por qué?

  Utilizo el comando `git reset --hard HEAD~1`ya que no solo queremos deshacer el último commit sino que también queremos _perder los cambios realizados en el working copy_, es por eso que `git reset HEAD~1` no nos sirve ya que _mantiene_ los cambios en el working copy.

- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?

  Ejecutamos `git reflog` para ver los movimientos de nuestro repo y utilizamos el comando `git reset --hard <numeroCommit>` recuperando todo aquello que había en ese commit.

- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?

  Hago el merge y en consola no me da ningún error, me ha mergeado correctamente ambas ramas y me muestra que han habido 9 inserciones y 10 eliminaciones en el archivo, sin embargo en github el merge parece no haber sido detectado ya que sigo teniendo el merge&pull request y los cambios no están en main. La consola también me notifica que mi rama (main) está por delante de origin/main por 1 commit.
  Ejecuto un ``git push ``para que el merge llegue a remoto. No hay ningún conflicto ya que el merge ha sido _fast forward_. _ME DOY CUENTA QUE HE REALIZADO EL MERGE AL REVÉS. MAIN HA ABSORBIDO A STYLED Y NO STYLED A MAIN_ volvemos a empezar.

  Me estoy volviendo majara. Intento hacer un ``git merge main`` pero me dice already up to date cuando realmente sabemos que no es así ya que el origin/head está en el commit anterior a styled así como main y origin/main. Con lo fácil que es hacerlo con github (cara que llora). Saco el ``git log--graph`` y evidentemente no está mergeado, entonces porque me dice que todo already up to date? Esto van a ser unas crónicas más que unas simples respuestas a las preguntas. ¿Es una pregunta trampa? ¿Este es el conflicto? No, el conflicto tiene que ser las lineas modificadas que tiene style que no están en main. Lloro. Empiezo a pensar que aquí hay trampa.
  
- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?

  Así que era trampa eh, madre mia no sabes tu las veces que he borrado y vuelto a hacer todo porque no entendía que diantres estaba pasando. El merge del paso 19 evidentemente causa conflicto porque htmlify tiene un código distinto al que tiene styled así que github nos llama y nos dice: "oye chavales, arreglad esto porque yo no trabajo gratis", y nos pone en pantalla los detalles de su crisis existencial.

- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?

  No ha habido conflicto porque es fast-forward

- ¿Qué comando o comandos utilizaste en el paso 25?

  ``git log --graph``

- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?

  Si, podría ser fast-forward porque la rama que se ha desvíado es htmlify y no title.

- ¿Qué comando o comandos utilizaste en el paso 27?

  ``git reset HEAD~1`` ya que _no queremos perder los cambios en el working copy_

- ¿Qué comando o comandos utilizaste en el paso 28?

  ``git reset --hard`` para descartar los cambios que estaban en el working copy

- ¿Qué comando o comandos utilizaste en el paso 29?

  ``git branch -d title`` y ``git branch -D title`` para confirmar que sabemos lo que hacemos

- ¿Qué comando o comandos utilizaste en el paso 30?

  ``git reflog`` para buscar el commit ID antes del merge
  ``git checkout -b tittle <commitID>`` para volver a crear la rama y restaurar todo
  ``git merge --no-ff title -m ""`` para volver a hacer el merge

- ¿Qué comando o comandos usaste en el paso 32?

  ``git log`` para ver el historial de commits
  ``git checkout <commitID>`` para volver al Initial commit

- ¿Qué comando o comandos usaste en el punto 33?

  ``git reflog`` ya que git log no nos sirve porque estamos en el commit inicial
  ``git checkout <commitID>`` para ir al último commit realizado, añado título
