- **¿Qué comando utilizaste en el paso 11? ¿Por qué?**
Para revertir al último commit utilicé el comando `git reset --hard HEAD~1`
- **¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?**
Primero utilicé el comando `git reflog` para acceder al hash del commit al que quiero regresar y luego con el comando `git redet --hard <hash>` volví a donde quería.
- **El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?**
Estando en la rama **Styled** al intentar hacer un merge con la rama **Main** obtuve un **"Already up to date"** debido a que la rama Styled está un commit por delante que la rama **Main**.
- **El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?**
Sí, hubo conflictos, debido a que en ambas ramas se han realizado cambios en las mismas líneas por lo que Git no sabe que hacer y nos obliga a resolver el problema manualmente.
- **El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?**
No, no causó conflictos, debido a que la rama **Styled** estaba un commit por delante que **Main** y **Main** no había avanzado mas allá de donde **Styled** estaba, por lo que simplemente se hizo un merge fast-forward moviendo el puntero de **Main** hacia el ultimo commit de **Styled**.
- **¿Qué comando o comandos utilizaste en el paso 25?**
Para realizar el diagrama usamos el comando principal `git -log` y agregamos las opciones: 
  * `--oneline` para mostrar solo la version corta del hash de cada commit y si mensaje.
  * `--graph` para dibujar un gráfico en ASCII con las ramas.
  * `--decorate` para que se muestren las ramas en la que se encuentra cada commit
  * `--all` para que no nos muestre solo el commit actual, sino todos.
En resumen sería el comando `git log --oneline --graph --decorate --all`
- **El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?**
Sí, porque la rama **Main** estaba un commit por detrás de **Title** y no había avanzada mas allá, por lo que se podría haber movido el punto hacia el ultimo commit de **Title** sin problema.
- **¿Qué comando o comandos utilizaste en el paso 27?**
Usé el comando `git reset --mixed 3c9a88a`, volviendo al commit anterior antes de realizar el merge, pero manteniendo el working copy intacto.
- **¿Qué comando o comandos utilizaste en el paso 28?**
Al haber usado en el paso anterior un `git reset --mixed` descartamos también los cambios del merge del staging area.
- **¿Qué comando o comandos utilizaste en el paso 29?**
Usé el comando `git branch -D title`
- **¿Qué comando o comandos utilizaste en el paso 30?**
Usé el comando `git reset --hard hash`.
- **¿Qué comando o comandos usaste en el paso 32?**
Primero usé el `git reflog`, tomé el hash del primer commit y luego hice uso de `git switch --detach hash`, aunque también puede ser `git checkout hash`
- **¿Qué comando o comandos usaste en el punto 33**
Al igual que antes solo moví mi puntero hacia el último commit.

