---
title: "De Scrum a Kanban — cómo entregamos tareas el doble de rápido"
date: 2019-03-21
draft: false
---

> *This post was originally published on [Medium](https://medium.com/@psluaces/scrum-a-kanban-2-veces-mas-rapido-f6c0802d93f1).*

Hemos reducido a la mitad el tiempo medio que tarda una tarea desde que se abre hasta que se pone en producción. De 7.52 a 3.66 días.

![](./1.png)

Y esta es la historia de lo que hemos hecho para conseguirlo.

No esperes recetas mágicas. Simplemente es que nos hemos centrado más en avanzar como equipo y menos en planes individuales.

### Contexto: 300 sprints y 13 años con Scrum

Hemos estado usando Scrum durante 300 sprints y más de 13 años. Aunque Scrum fue bueno, de algún modo dejó de funcionarnos. Así que pensamos que podríamos poner más énfasis en colaborar como equipo y decidimos movernos a Kanban.

### El libro que lo cambió todo

Unos cuantos meses antes de movernos, nos leímos unos cuantos libros sobre Kanban.

Pero hubo uno que nos gustó especialmente.

Se trata de “Agile Project Management with Kanban” de Eric Brechner (que la verdad es que tiene otros libros muy buenos también).

La verdad es que ya no sé si un libro es realmente bueno o malo, o es que depende de en qué momento te pille. En todo caso, este llegó en el momento correcto, al menos para mí.

El libro de Brenchner explica Kanban de una forma muy práctica y analítica. Y eso fue exactamente lo que me gustó. No va tanto de ensalzar la colaboración casi en plan místico como otros, sino que va directo al grano.

### De qué va Kanban — al menos en mi cabeza

Cuando dices Kanban la primera imagen que te viene a la cabeza suele ser un tablón y post-its pegados.

Bueno, para mí ya no es solo eso.

Kanban va de limitar el trabajo en progreso (work in progress o WIP).

Limita el número de tareas abiertas, y el equipo entero se centrará en moverlas adelante para poder meter otras, en lugar de en sus planes individuales.

### Cycle time vs lead time

Esto lo explica muy bien el libro.

El “cycle time” es el tiempo que pasa desde que abres una tara hasta que se pone en producción.

![](./2.png)

El “lead time”, sin embargo, es el tiempo que pasa desde que la tarea o bug se mete en el sistema.

Nosotros no nos hemos centrado en medir el lead time, aunque en soporte sí que lo consideramos.

### Herramientas

Bueno, por supuesto usamos Plastic SCM como nuestro control de versiones y usamos “branch per task” para implementar cada tarea (y tenemos un libro gratis que te puedes descargar en PDF o leer online y que va justo de esto: “Version Control, DevOps and Agile Development with Plastic SCM”: [https://www.plasticscm.com/documentation](https://www.plasticscm.com/documentation)).

Usamos también nuestro propio gestor de tareas (que tiene más años que la empresa) para cada bug y para cada nueva feature (no escribimos ni una línea de código sin tener una tarea asociada).

Pero, sí, necesitábamos una buena herramienta para montar el tablón Kanban.

Estas son las que evalué:

**Jira**

[https://www.atlassian.com/software/jira/features](https://www.atlassian.com/software/jira/features)

Price: $7/user/month

Tiene WIP limits — [https://www.atlassian.com/agile/tutorials/how-to-do-kanban-with-jira-software](https://www.atlassian.com/agile/tutorials/how-to-do-kanban-with-jira-software)

Pero no vi que soportase múltiples columnas, que es algo que recomienda Brechner.

**Kanbanflow**

[https://kanbanflow.com](https://kanbanflow.com/)

Free (limited). $5/user/mo (more features, analytics, integrations)

También tiene WIP limits.

Les pregunté si podían hacer lo de multi-column pero parece que no.

**Kanbanize**

[https://kanbanize.com/software-development](https://kanbanize.com/software-development)

$148/mo for up to 15

Su web me pareció poco clara.

**Leankit**

[https://leankit.com](https://leankit.com/)

$19/user/mo or $32/user/mo

No me gusto su interfaz web.

Parece que sí que es de las pocas que puede hacer multi-colum WIP limit.

**Kanbantool**

[https://kanbantool.com](https://kanbantool.com/)

$3.5/user/mo or $6.5/user/mo

No estoy seguro de que pueda hacer WIP limits.

**Kanbantree**

[https://kantree.io](https://kantree.io/)

7 eur/user/mo

Parece que es una pequeña empresa francesa, lo que me gustó mucho.

Pero no veo que tengan lo de las multi-lines.

**Realtimeboard — ahora Miro**

Bueno, pues al final nos decidimos por Realtimeboard (que acaban de renombrar a Miro hace unas pocas semanas). No es una herramienta Kanban en realidad, y no proporciona ninguna característica avanzada para forzar los WIP limits, y hasta es más cara que las otras.

Pero… a mí me gustó mucho más, por unos cuantos motivos.

Este es el tablón que propone el libro:

![](./3.png)

Te recomienda poner WIP limits que afecten a dos columnas o más dentro de la misma fase.

Mira la fase “implement”: tiene dos columnas. La primera significa tareas abiertas, y la segunda tareas terminadas de implementar (y listas para pasar a la siguiente fase). Sin embargo el límite para ambas es de 5.

Eso quiere decir que podrías tener 3 tareas abiertas, pero si hay 2, como en el dibujo, listas para pasar a la siguiente fase, entonces no puedes meter más.

El límite de trabajo en progreso afecta a la vez a “open” y a “done”.

Casi todas las herramientas que he revisado no podían hacer esto. Todas parecen centradas en fijar el WIP limit por columna, pero entonces no consigues el mismo efecto. Es decir, un WIP de 3 on “implement-open” y otro de 2 en “implement-done” no es lo mismo que un límite global de 5 afectando a ambas columnas.

Esto me pareció muy importante y por eso no propuse ninguna de las otras herramientas.

Además, Realtimeboard/Miro nos da mucha flexibilidad. Es lo más parecido a tener un tablón físico porque al final estamos muy distribuidos y una pizarra no nos iba a funcionar. Vale, no trae ninguna automatización de ningún tipo, tenemos que mover las tarjetas nosotros… pero, ¿no es justo eso de lo que va Kanban?

Unas pocas semanas después de movernos a Kanban nos cambiamos también a Basecamp para toda nuestra comunicación interna. Redujimos de forma drástica el uso de Slack (la fuente de interrupciones más grande conocida después de un teléfono sonando) y también del email, y ahora tenemos un sitio estupendo para hablar de nuevas features y de bugs y todo queda registrado. Podemos meter un link a una conversación de Basecamp en nuestro issue tracker cuando finalmente decidimos implementar aquello de lo que estuvimos discutiendo. Solo esto, por simple que parezca, es una pasada, porque no consigues lo mismo si la discusión está por email. También evaluamos Twist, pero al final nos quedamos con Basecamp.

### Nuestro tablón Kanban

Pues esta es la pinta que tiene nuestro tablón Kanban en Miro (realtimeboard).

![](./4.png)

Hicimos unos pocos cambios respecto a lo que proponía el libro, pero en esencia es lo mismo.

· **Backlog**. No fijamos WIP limits para el backlog y tampoco dividimos en “en progreso” y “especificado”. Lo hicimos durante unas semanas, pero no nos encajaba así que al final lo borramos. Tenemos margen de mejora aquí.

· **Implement**. Tres columnas: open, locked y done. Locked debería ser una excepción: solo debería tener tareas que no puedan progresar por una buena razón. Deberían ser pocas y no cuentan en el WIP limit. La verdad es que a veces, como en la captura, abusamos un poco de ella, para desesperación de todos. Las columnas “open” y “done” son muy claras: tareas en progreso o terminadas pero pendientes de revisar y validar.

· **Review.** Revisamos cada tarea, y dividimos la fase en “en progreso” y “hecho”. Las dos cuentan para el WIP limit.

· **Validate.** Solo la “in-progress” cuenta para el WIP limit. Basicamente muestra tareas que es están validando \*ahora mismo\*.

· **Deploy.** Esta es la que más ha crecido. Tenemos una columna inicial “merged” que significa que la tarea ya fue integrada en main pero no es todavía parte de una release. El cycle time sigue corriendo. Luego tenemos una columna “deploy” para cada uno de los productos que mantenemos: Plastic y la web plasticscm.com, semantic con su web, y gmaster con su web. Una vez están en deploy, el cicle time deja de contar.

Una vez que una tarea llega a “validate done” entra en modo automático. Un mergebot ([https://www.plasticscm.com/mergebot-devops](https://www.plasticscm.com/mergebot-devops)) se encarga de hacer el merge con main (y dejar ese merge en un sitio temporal), lanzar el build, lanzar los tests, confirmar el merge (desde ese sitio temporal) y preparar la nueva versión para release.

Cualquiera de esas acciones automáticas podría fallar, y si pasa, la tarea vuelve a “implement open”.

Todos esos cambios de estado los hacemos a mano, de una forma colaborativa (el primero que lo ve, lo mueve). Vale, sí, es un dolor a veces, pero nos obliga a estar atentos y al día de lo que está pasando, que es exactamente lo que queríamos.

No voy a contar aquí cómo hemos calculado los WIP limits porque da para otro blogpost, y además el libro de Brechner lo explica muy bien.

Lo que probablemente sí que merece la pena es explicar cómo usamos las tarjetas:

![](./5.png)

### ¿Qué nos motivó a cambiar?

Cuando fundé Códice, allá por 2005, ya era un creyente en Peopleware. Esto quiere decir que incluso montamos la oficina de acuerdo a lo que el libro recomendaba. Un mínimo de metros cuadrados por persona, mucho silencio, nada de cubículos y tampoco pasarnos con los espacios abiertos.

Este es un plano de nuestra oficina en Boecillo.

![](./6.png)

Del mismo modo que lo intenté con el código y con todo lo demás, era mi oportunidad de “hacer las cosas bien”.

Por supuesto, cometí un montón de errores, pero creo que con la oficina no salió mal.

Y una de las cosas que Peopleware recomendaba era que encontrásemos una buena forma de trabajar.

Así que Scrum vino al rescate. Para mí, con menos de 30 años y unos 5 años de experiencia, me vino estupendo. Me había leído el libro de Schawber “Agile Project Management with Scrum” y comenzamos a aplicarlo inmediatamente. Dos reuniones al principio, lista de tareas, el daily, review y retrospectiva. Vamos, que pasas de cero a tener al equipo ocupado y organizado en nada. Me encantaba.

Durante un par de años le dimos vueltas a la duración de los sprints. Empezamos con 4 semanas, pero después de la segunda siempre cambiábamos planes. Así que finalmente lo dejamos en 2 semanas por sprint y hemos medido el tiempo de esa forma desde entonces. Durante más de 12 años. Y todavía usamos “sprints” para saber dónde estamos aunque ya no tenga tanto sentido en Kanban.

¿Qué es lo que fue mal? Bueno, yo no diría que hay nada roto con Scrum. Fuimos nosotros, no Scrum :P.

· Una release al final del Sprint siempre nos resultó raro. Desde casi el principio intentamos hacer siempre al menos una release por semana, y el objetivo era hacer muchas más. Esto quiere decir que incluso cuando estábamos a tope con Scrum, el final del sprint tampoco significaba mucho.

· Al principio todo lo del sprint planning nos encantaba. Pero unos años más adelante, ya con un equipo menos homogéneo (¡que no es malo!), algunas discusiones sobre qué iba primero y qué después tenían menos sentido. A ver, que siempre ha opinado todo el mundo, no es eso, pero había temas que teníamos ya trillados y que no daban para otra conversación. Hemos vuelto un poco a esto recientemente, hemos probado discutir más y menos a lo largo del tiempo.

· Las retrospectivas y las reviews nos gustaban al principio. Guardamos notas de todas las que hicimos bien ordenada en nuestra wiki interna. Pero muchos, muchos meses después comenzó a parecernos burocracia. Era obligatorio hacerlo. Sí, sin duda el problema éramos nosotros, pero teníamos más ganas de sacar trabajo adelante que de discusiones filosóficas cada dos semanas. Quizá es que el tamaño de los sprints estaba mal.

· Nunca implementamos lo de la velocity. Siempre estimamos en “ideal days”, nunca en story points. Culpa mía. Lo asumo, pero la realidad es que nunca lo hicimos.

· Optimizamos todo para productividad individual. A ver, es algo bueno. Minimizar el ruido (soy un gran fan también de “Pragmatic Learning and Thinking” y los autores insisten en que llevar auriculares mata la creatividad. Por eso siempre quiero que el espacio de trabajo no tenga mucha gente, y que sea lo más silencioso posible. Escuchar música debe ser una opción, pero no obligatorio para que no te molesten), reducir interrupciones (notificaciones deshabilitadas, no interrumpir a la gente en su mesa), salas de reuniones fuera de la zona de trabajo, y todo eso.

Voy a profundizar un poco más en lo de “productividad” porque probablemente sea la principal causa de por qué necesitamos cambiar.

Añade una década entera a esas ideas sobre colaboración, y al final nos convertimos en maestros de “estar en flow”. Pero entonces algo se nos fue de las manos…

“Eso no está en mi plan”.

Tengo la suerte de contar con un equipo con gente siempre encantada de echar una mano y que además ha estado trabajando junta durante muchos años (llamamos “nuevo” todavía a los que llevan aquí ya 5 años!).

Yo siempre he intentado hacer todo lo posible para seguir esas reglas de Peopleware, pero la parte mala es que en un momento dado comenzamos a primar los planes individuales sobre los del equipo.

Al principio de cada sprint cada uno tenía su lista de tareas. Crear esa lista se convirtió en un auténtico dolor también, y hablaré de ello luego. Esa lista de tareas era EL objetivo del sprint. No es que pasase nada si no terminásemos la lista, muchas veces no lo hacíamos, pero era a lo que aspirábamos.

Y entender lo que era importante a nivel global se hizo cada vez más difícil. Es decir, cada uno estaba con su lista y quizá estaba a tope con su tarea en lugar de echar una mano a alguien con otra más importante.

Por supuesto, no puedo decir que esto fuera culpa de Scrum, era culpa mía. Pero es lo que ocurrió.

Algo más sobre las tediosas “lista de tareas”. En nuestra búsqueda de la máxima productividad individual, comenzamos a considerar los meetings como un mal necesario. Y probablemente fuimos demasiado lejos. Siempre hemos hecho reuniones de plan cuando era necesario, pero al final yo me encargaba de preparar una lista de tareas para cada uno, con ayuda de unos pocos del equipo. Esto ahorraba mucho trabajo “administrativo” a todos. Por supuesto todos entedíamos siempre la dirección global, pero la mayoría estaba a salvo del trabajo burocrático. ¿Fue bueno? Pues no lo sé, el caso es que el tiempo dedicado a plan comenzó a subir.

Un cálculo rápido de las horas totales dedicadas a “plan” en Scrum: 4 horas máximo de reuniones de plan + 1hora de review y otra de retrospectiva al final = 6h x 10 personas = 60h de plan cada dos semanas para un equipo de 10.

La verdad es que nunca llegamos al máximo de 60 horas, pero sí hemos estado muchas veces en 30–40 y lo considerábamos terrible. Quizá somos exagerados, pero no nos gustaba nada.

Así que intentamos encontrar una forma mejor de trabajar.

¡Ah! ¡Otra cosa más! La mayoría del equipo odia los daily meetings. Empezamos a hacerlos a primera hora de la mañana hace mil años. Pero “primera hora” variaba mucho, especialmente al principio, cuando algunos (entonces veinteañeros) llegaban a las 10:30. A medida que pasan los años parece que todos prefieren llegar antes e irse también antes. Bueno, que al final movimos “primera hora” a “cuando se pueda” y finalmente lo estandarizamos en “antes de comer”. Y nos mantuvimos en eso durante años. Y parecía funcionar. Hicimos todo lo posible para mantenernos en 15 minutos máximo. Y aunque hubo algún año malo, en 2017 y 2018 los acortamos mucho y nos mantuvimos en esos límites.

En todo caso, los seguimos haciendo porque… bueno, porque parecía lo correcto. Pero muchas veces no escuchábamos del todo, o las explicaciones eran pobres. Intentamos hacer todo lo possible para comunicarnos mejor.

Pero, al final, no dejaban de ser reuniones, y no nos gustan las reuniones, así que al pasar a Kanban dejamos de hacerlas.

### ¿Cómo hicimos el cambio?

Pues me releí el libro de Eric Brechner en detalle y preparé una presentación para explicarlo todo al equipo, destacando lo que consideraba clave. El primer día del Sprint 294 hice la presentación a todos y nos pusimos luego a calcular los WIP limits juntos durante unas horas. El Realtimeboard ya lo tenia preparado.

Y ya está. Comenzamos a usarlo sin más. La primera semana ya nos gustó, y en la segunda el cycle time ya era mejor que en los últimos sprints de Scrum, y no ha empeorado desde entonces.

### ¿Qué ha ido bien?

Más trabajo terminado, menos reuniones, menos tiempo dedicado a “cosas de plan” (de 30–40 horas por sprint a tan solo 5 horas en muchos de los nuevos, y con picos de 20 horas que ahora consideramos horribles cuando antes era normal).

La sensación de progreso, de avance y de trabajo en equipo es mucho mejor cuando colaboramos en mover tareas.

### ¿Qué necesita mejora?

Lo primero que se me ocurre es la columna de Backlog. Sí, tenemos un roadmap bien hecho, y listas y de todo, pero podemos hacerlo mejor en el tablón Kanban.

### ¡Números!

He recopilado algunos números (gracias a nuestro issue tracker) de los últimos sprints con Scrum y de los más recientes con Kanban para comparar:

![](./7.png)

“Cycle time” es el tiempo en días que pasa desde que una tarea se empieza hasta que está en release.

“Net cycle time” es lo mismo, pero quitando fines de semana (más realista, menos pesimista).

Lo más destacable comparando los últimos 4 sprints (2 semanas cada uno) de Scrum y los 4 más recientes de Kanban:

· Hemos reducido el net cycle time medio de 7.52 días a 3.66. Es ser 2 veces más rápidos.

· Contando fines de semana (cycle time) hemos pasado de 9.38 a 4.40 días. 2.1 veces más rápido.

Si os dais cuenta, no es que hagamos mucho más trabajo, es que simplemente lo ordenamos de forma diferente.

Otros números que me parecen muy interesantes son los del tiempo dedicado a tareas de plan. Se ven en la siguiente tabla:

![](./8.png)

El SPRINT 294 fue el primero de Kanban.

Horas en planning en los 14 útimos sprints de Scrum = 440h (5% del tiempo total de trabajo).

Horas en planning en los siguientes 14 spritns con Kanban = 180h (3% del tiempo total).

Vamos, que hemos reducido burocracia a la mitad.

Y esto no cuenta el tiempo de los “daily standups” que tampoco solemos hacer (cada uno cuenta lo que ha hecho al final del día en Basecamp en algo que llaman “daily checkins”).

De media estábamos gastando 31h de plan cada 2 semanas. Ahora gastamos 13.91. Eso son 17h menos de media cada dos semanas. Como normalmente consideramos 60 horas productivas (o incluso algo menos) es como haber añadido 0.28 nuevos miembros al equipo.

(No cuentes mucho las horas totales, porque han estado las navidades y también ha llegado nueva gente al equipo).

En caso de que quieras saber qué significan las otras columnas: “dev” significa tiempo de desarrollo, “rev” tiempo de code reviews, y “val” tiempo de validaciones.

### A veces el propio hecho de cambiar ya ayuda…

A pesar del título del blogpost, no le echo la culpa a Scrum. Nos funcionó muy bien durante más de una década, y probablemente ha sido culpa nuestra no haberlo usado mejor. Ahora veo claro que durante tantos años lo fuimos alterando y cometiendo errores, y hay cosas que nunca dominamos.

Pero lo que considero importante es que a veces cambiar de hábitos ayuda mucho. Cambiamos nuestra forma de trabajar y encontramos algo que nos gustó más y que cumplía con lo que buscábamos: trabajar mejor como equipo.

A veces el cambio es lo que importa, salir de la rutina. No es que Kanban no sea bueno, me encanta, pero me pregunto cuánto de la mejora viene realmente del método y cuánto de ilusionarnos con algo nuevo.
