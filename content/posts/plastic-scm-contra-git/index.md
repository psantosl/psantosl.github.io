---
title: "Plastic SCM contra Git"
date: 2018-03-13
draft: false
---

> *This post was originally published on [Medium](https://medium.com/@psluaces/plasticscmvsgit-e226ff50c01).*

(This blogpost is available in English [here](https://medium.com/@psluaces/plasticscm-vs-git-c17934fad7ed)).

Hay una pregunta ineludible cada vez que voy a un meetup o a una conferencia y alguien se entera de que desarrollo Plastic SCM: ¿cómo se compara con Git? Muchos me lo preguntan por pura curiosidad o interés; otros, me da la impresión de que casi ofendidos de que osemos a desafiar al sistema dominante concebido por el mismísimo Torvalds. Es casi en plan “¿qué podéis hacer vosotros, pringadillos, contra EL sistema dominante? Y, además, ahora está apoyado por Atlassian, Microsoft, GitHub, GitLab y otras multinacionales que tienen más gente en la recepción que vosotros en desarrollo.”

Bueno, pues eso es lo que voy a explicar: ¿qué hace diferente a Plastic de Git que hace que podamos tener clientes con más de 2500 desarrolladores usándolo, pequeños estudios de videojuegos, grandes estudios, empresas de automoción, seguros, aeroespacial y muchos otros? ¿Estarán todos locos?

![](./1.jpeg)

Somos casi como Astérix y Obélix resistiendo contra el imperio. ;-)

### Ramas de verdad

En Plastic las ramas son contenedores de changesets (commits en jerga Git). En Git las ramas son punteros a un commit.

¿Qué quiere decir esto? Que en Plastic una rama es como te la imaginas en tu cabeza: una línea de trabajo, con muchos checkins. Un changeset, como nosotros le llamamos, no puede estar en varias ramas, solamente en una. Fácil y sencillo.

En Git tienes que adaptar tu cabeza a pensar en su formato de punteros, y muchas veces no es nada fácil saber dónde se hizo un commit. Y puedes decir, vale, ¡y qué más da! Pero, ¿a que cuando ves un blame te gustaría saber en qué tarea se tocó una línea sin tener que volverte loco o depender de los mensajes de commit? Pues eso te lo dan las ramas de Plastic.

![](./2.png)

Además, en Git es muy habitual “borrar ramas” porque estorban, sin más; algo que en Plastic no haces. Se hace también porque la mayoría de las GUIs de Git (la línea de comandos no), se mueren directamente si tienes un repositorio con 2mil ramas. Si haces una rama por tarea, como recomendamos nosotros, puedes tener repositorios con 10mil, 20mil ramas… y no es ningún problema en Plastic.

Una cosa más: como te decía, en Git puedes dejar de saber fácilmente qué pertenecía a qué rama, mientras que en Plastic no:

![](./3.png)

¿Es muy importante esto? Implica trazabilidad total y facilidad de uso. No conozco a un solo instructor de Git que no te diga que tiene que amueblar la cabeza de los alumnos para que piensen en punteros y no en ramas “normales”. En Plastic es más intuitivo, sin más.

### Trabajar centralizado

Con Plastic puedes tener tu repositorio local y trabajar en distribuido, como en Git. Pero también puedes trabajar tipo Subversion: con una copia local y haciendo checkin contra el servidor directamente, sin pasos intermedios. Y no, Git no puede hacer eso: siempre necesitas un repositorio local.

¿Cómo es de importante esta flexibilidad? Tener un repositorio local es superútil para mucha gente, les encanta; pero para otros es una pesadilla. Es hacer “checkin y ya está”, contra “checkin y luego push”.

En general, los artistas en estudios de videojuegos prefieren trabajar en central y dejarse de que el control de versiones les pueda amargar la vida (entendiendo por artistas todos los que no son programadores, que pueden ser diseñadores de juego (los que piensan la mecánica y la jugabilidad), animadores, modeladores 3D, artistas gráficos).

Nos encontramos también con muchos programadores que, con redes que vuelan en la oficina, prefieren centralizado. Plastic no es como SVN. Es fortísimo con ramas y merges, como Git o más. Por tanto, el hecho de trabajar centralizado no te quita esa potencia para nada. Recuerda que mucha gente lo que realmente valora de Git es branching/merging, mucho más que ser distribuido.

### Plastic no llora con grandes repositorios

Tenemos clientes con repositorios de 5TB. No puedes hacer eso en Git. Vale, hace unos días estábamos con desarrolladores de GitLab/Hub y nos decían “es que si un repositorio es tan grande es que tiene cosas que no deberían estar ahí”. A ver, tienes un proyecto de videojuegos, o de automoción, y gestionas ficheros grandes. Y le dices a tu cliente que meta el código en Git y que los binarios los meta en… ¿Dropbox? Bueno, pues parece que eso convence a muchos.

En Plastic simplemente le puedes hacer checkin y listo. No se rompe, no le pasa nada. No necesita apaños tipo LFS (de los que todos los usuarios Git que lo usan quieren huir antes o después). Está diseñado para que le metas de todo y funcionar, sin dramas.

Esto nos permite trabajar con muchísimos estudios de videojuegos, ya sea gestionando el trabajo de +300 artistas como en Telltale, o grupos indie con poca gente, pero mucho contenido.

Lo mismo aplica a nuestro Cloud: GitHub te pide amablemente que quites tu repositorio si pasa de 2GB. En Plastic Cloud la media son +50GB.

### Versionado de directorios y movidos

Esta es otra diferencia basada en un diseño diferente entre Git y Plastic, y se explica muy fácil: renombra un directorio con 1000 ficheros en Git, y verás 1000 ficheros movidos. Haz lo mismo en Plastic y verás un directorio renombrado. Más fácil de entender. Vamos, lo de Git es nivel dolor de cabeza en vez de lo que esperas que haga un control de versiones.

Versionar directorios nos complica la vida a nivel de implementación, pero nos deja trazar los renombrados y movidos de forma precisa, lo que te salva la vida una y otra vez en merges complicados y en diffs.

### Visualización, GUIs, todo de serie

Esto de la visualización y las GUIs ya lo tengo tan interiorizado que muchas veces se me olvida contarlo. Lo doy por hecho. Pero tiene mucha importancia.

Cuando instalas Plastic viene “de serie” una interfaz gráfica de usuario muy completa y muy centrada en visualización. No voy a poner capturas de pantalla aquí, pero puedes ver [nuestra gallery](https://www.plasticscm.com/gallery.html) y una de las características más importantes, el [Branch Explorer](https://www.plasticscm.com/branch-explorer/index.html).

Al final es un trabajo enorme hacer el core del servidor, el cliente, las GUIs, integraciones… de todo. Pero el resultado es un producto muy consistente, o mucho más que cuando en Git muchas GUIs son wrappers de la línea de comandos y cuando te sale un merge te dice “error, merge detected” que ya te echa para atrás.

En el paquete vienen cosas como [mergetools](https://www.plasticscm.com/features/xmerge.html) (con detección de movidos, bastante único), de modo que no tienes que hacer diff o merge de texto o instalarte un Kdiff3. También trae de serie side-by-side diff, algo que todavía hoy muchas GUIs de Git no incluyen. Y luego añadimos cosas que nadie tiene como “[semantic version control](https://www.plasticscm.com/features/semantic-version-control.html)”.

### Y puede interactuar con Git

Cualquier cliente de Plastic puede hacer push/pull contra un servidor de Git, y cualquier servidor de Plastic puede recibir push/pull de Gits (que se piensan que hablan con otro Git). Está explicado [aquí](https://www.plasticscm.com/features/plasticscm-for-git-users.html) y da mucha flexibilidad para equipos que se están moviendo desde Git a Plastic o necesitan interactuar con otros grupos externos en Git.

### Para terminar

Como te decía al principio, la pregunta de “cómo os comparáis con Git” es muy, muy frecuente, así que espero haber explicado cómo nos diferenciamos a día de hoy.

Todo se resume en:

· ramas más fáciles de entender,  
· merges todavía más potentes,  
· grandes repositorios y grandes ficheros,  
· visualización.

Así que, si eres un fan de Plastic, espero haberte dado argumentos para contratacar cuando te ataque el próximo soldado git-imperial ;-)
