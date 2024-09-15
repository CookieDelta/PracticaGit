Práctica Git & GitHub
Información de contacto del profesor:

Alberto Casero kas.appeal@gmail.com

Ejercicio 1
Se deberá crear un repositorio y realizar una serie de operacionesdesde la consola de comandossobre el mismo para posteriormente subir el repositorio a Github.

Se deberá entregar a través del formulario de prácticas indicando la URL del repositorio. En el repositorio, deberá existir un archivo readme.md con las respuestas a las siguientes preguntas:

-	¿Qué comando utilizaste en el paso 11? ¿Por qué?

git reset --hard HEAD~1
Porque debía limpiar el working copy y además volver el head al commit anterior

-	¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?

git reset --hard HEAD@{1} que quiere decir que se limpia el área de trabajo y se vuelkve el puntero HEAD al commit inmediatamente anterior (por eso el {1})

-	El merge del paso 13, ¿Causó algún conﬂicto? ¿Por qué?

No, porque se tomó como una actualización del archivo git-nuestro que estaba en otro paso más adelante, en otro commit


-	El merge del paso 19, ¿Causó algún conﬂicto? ¿Por qué?

Si, pues habian dos versiones distintas del archivo que debían "unirse", se debió dejar la rama styled como se mencionó en el enunciado

-	El merge del paso 21, ¿Causó algún conﬂicto? ¿Por qué?

No, porque se tomó como una actualización del archivo git-nuestro que estaba en otro paso más adelante, en otro commit

-	¿Qué comando o comandos utilizaste en el paso 25?

git log --graph y me muestra el grafo con las branches del proyecto

-	El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?

Si, porque se puede tomar como un avance de la rama anterior

-	¿Qué comando o comandos utilizaste en el paso 27?

git reset --soft HEAD~1

-	¿Qué comando o comandos utilizaste en el paso 28?

git checkout --git-nuestro.md

-	¿Qué comando o comandos utilizaste en el paso 29?

git branch -D title

-	¿Qué comando o comandos utilizaste en el paso 30?

Se debe ir hacia la rama title por git reflog, pues está eliminada, se ubica su identificador que es 4ad598f
git merge 4ad598f

-	¿Qué comando o comandos usaste en el paso 32?

git log para ver el identificador del primer commit, luego git checkout cd28bd8

-	¿Qué comando o comandos usaste en el punto 33?

git log para ver el identificador del último commit, luego git checkout 4ad598f

Los pasos a ejecutar son los siguientes (los pasos en negrita indican que hay una pregunta asociada):

1)	Crear un repositorio en GitHub y clónalo en tu equipo
Done
2)	Crear un archivo git-nuestro.md con el contenido:

Git nuestro

Git nuestro que estas en los repos Comprimidos sean tus commits Venga a nosotros tu log
En el local como en el remote Danos hoy nuestro pull de cada día Perdona nuestros conflictos
Como también perdonamos los de otros geeks No nos dejes caer en detached HEAD
y líbranos de SVN git commit --amend
Done
3)	Añadir git-nuestro.md al staging area
Done
4)	Mover lo que hay en el staging area al repositorio
Done
5)	Crear una rama llamada “styled”
Done
6)	Listar las ramas que hay en el repositorio
Done
7)	Moverse a la rama “styled”
Done
8)	Comprobar que se está en la rama correcta
Done
9)	Modiﬁcar en el archivogit-nuestro.md:
Done
*Git* nuestro que estás en los repos Comprimidos sean tus *commits* Venga a nosotros tu *log*
En el local como en el *remote* Danos hoy nuestro *pull* de cada día Perdona nuestros *conflictos*
 
Como también perdonamos los de otros geeks No nos dejes caer en *detached HEAD*
y líbranos de *SVN*

`git commit --amend`

10)	Añadir los cambios al staging area y luego pasarlos al repositorio
Done
git push --set-upstream origin styled
11)	Deshacer el último commit (perdiendo los cambios realizados en el working copy)
Done
git reset --hard HEAD~1

12)	Rehacer el último commit (el que acabamos de deshacer)
git reset --hard HEAD@{1}
13)	Hacer un merge con ‘main’ (styled absorbe a main)
primero revisar que estemos en la Branch styled
git Branch
luego merge main into styled
git merge main
14)	Volver a la rama main

15)	Crear una nueva rama llamada “htmlify”

16)	Cambiar a la rama htmlify

17)	Modiﬁcar en el archivogit-nuestro.md:

<p><em>Git</em> nuestro que estas en los repos<br /> Comprimidos sean tus <em>commits</em><br /> Venga a nosotros tu <em>log</em><br />
En el local como en el <em>remote</em><br /> Danos hoy nuestro <em>pull</em> de cada día<br /> Perdona nuestros <em>conflictos</em><br />
Como también perdonamos los de otros geeks<br />

No nos dejes caer en <em>detached HEAD</em><br /> y líbranos de <em>SVN</em><br />
<code>git commit --amend</code></p>

18)	Hacer un commit

19)	Hacer un merge de “htmlify” en “styled” (styled absorbe a htmlify)

20)	Si hay conﬂictos, deberemos resolverlos quedándonos con el contenido de la rama “styled”.

21)	Desde “main”, hacer un merge con “styled”

22)	Crear una rama “title” y cambiarse a esa rama

23)	Añadir un título (a tu gusto) al archivogit-nuestro.mdy hacer un commit.
 
24)	Volver a la rama main 

25) Dibujar el diagrama
git log --graph
26)	Hacer un merge “no fast-forward” de “title” en “main” (main absorbe a title)
git merge --no-ff title
27)	Deshacer el merge (sin perder los cambios del working copy)

git reset --soft HEAD~1

28)	Descartar los cambios

git checkout -- git-nuestro.md

29)	Eliminar la rama “title”

30)	Rehacer el merge que hemos deshecho

Se debe ir hacia la rama title por git reflog, pues está eliminada, se ubica su identificador que es 4ad598f
git merge 4ad598f

31)	Volver a main y eliminar el resto de ramas 


32) Volver al commit inicial cuando se creó el poema
git reflog
git checkout cd28bd8
33)	Volver al estado ﬁnal, cuando pusimos título al poema
git checkout 4ad598f
git checkout -b title_again para salir de detached head

34)	Crear los siguientes tags: 
inicial: en el primer commit
styled: modiﬁcación del paso 10 
htmlify: modiﬁcación del paso 17-18 
title: modiﬁcación del paso 30

35)	Ir al tag htmlify

36)	Vuelve a la rama main

37)	Sube a GitHub todas las ramas y todos los tags
