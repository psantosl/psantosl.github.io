---
title: "Únete al equipo de Core de Plastic SCM en Unity"
date: 2021-09-09
draft: false
---

> *This post was originally published on [Medium](https://medium.com/@psluaces/%C3%BAnete-al-equipo-de-core-de-plastic-scm-en-unity-9b11a3521101).*

Estamos buscando a una **ingeniera o ingeniero** para el equipo de **Core** de Plastic SCM. Alguien con mucha experiencia que nos ayude a reforzar el equipo.

Esta es la oferta oficial: [https://careers.unity.com/position/senior-software-engineer/3281173](https://careers.unity.com/position/senior-software-engineer/3281173)

En este blog post voy a intentar contar más sobre el puesto, el trabajo, el equipo, para darle más color, además en español, y así que te animes a mandarnos tu currículum.

![](./1.png)

### Qué es el equipo de Core de Plastic SCM

Hasta finales de 2020 en Plastic éramos un único equipo que hacía de todo. Por supuesto había gente que sabía más de GUI que de algorimos de merge, o de IntelliJ y cómo integrarse que de sockets, pero uno de los atractivos era que todos tocábamos todo. El espíritu sigue ahí, pero hemos pasado de 10 personas en desarrollo a un grupo de casi 40… y creciendo… mucho.

Así que hemos cambiado la forma de organizarnos.

Ahora somos estos equipos:

· Core

· Desktop

· Support

· Integrations

· Plugin

· WebUI

Y el equipo de Core se encarga de muchas cosas diferentes que son, como dice la palabra, muy del núcleo: el servidor de Plastic, ya sea el que va en cada portátil cuando te lo instalas, el que se despliega en entornos corporativos para atender a miles de usuarios, o el cloud con el que atendemos a muchos miles en Cloud (y en China cientos de miles :P).

Es el equipo que se encarga de todo lo interno del sistema:

· Rendimiento, red, memoria.

· Línea de comandos (aunque no es el único equipo que lo toca).

· Nuestro sistema interno de devops.

· Cloud.

· Server(s).

· Sistema de merge, incluyendo algorimos, pero sin incluir nuestra merge tool ni semanticmerge (eso es de Desktop, aunque tenemos gente en este equipo que se sabe todo de esos sistemas).

### Quiénes trabajan en Core

Hemos tenido la suerte de que se nos hayan ido muy pocos desarrolladores del grupo a lo largo de todos estos años, y eso quiere decir que tenemos gente con muchísima experiencia.

Algunos de los compañeros con los que trabajarás: [Rubén](https://www.plasticscm.com/company/team#ruben-de-alba) que se unió en 2006 y ha desarrollado de todo, desde concurrencia a tests GUI, algorimos de merge, etc. [Borja](https://www.plasticscm.com/company/team#borja-ruiz) una de nuestras superestrellas, el cerebro detrás del sistema de merge, nadie lo entiende como él. [Jesús](https://www.plasticscm.com/company/team#jesus-gonzalez), creador de nuestro sistema de devops que finalmente productizamos con el nombre de mergebots. [Sergio](https://www.plasticscm.com/company/team#sergio-luis), que lleva en el equipo desde 2015 y ha hecho de todo, y arrancó portando el código cliente de Plastic a un Android. Y siguen incorporaciones más recientes que puedes encontrar en la página de Team como Ryan (que viene de otro equpo de Unity), Mikel, Jaime…

### Qué te podemos ofrecer en Core

Un reto enorme. No te vas a aburrir. ¿Quieres hacer algo que ni Git es capaz de hacer? Este es el sitio.

Unos compañeros que te llevarán de la mano hasta que te encuentres a gusto.

Algunas de las cosas espectaculares que han hecho recientemente:

· Un virtual filesystem versionado! Esto es de lo más hacker que se puede hacer: escribes en el filesystem, y se versiona solo, y se baja ficheros (checkout si usas git) bajo demanda… pero con un algorimo de ML para optimizar la descarga. Una pasada! Aquí puedes leer un [blogpost entero](https://blog.plasticscm.com/2021/07/dynamic-workspaces-alpha-for-windows.html) sobre el tema. Y un thread de twitter más ligero y en español, [aquí](https://twitter.com/psluaces/status/1420869289352089609).

· Se encargan de todo Plastic Cloud, servidor superescalable, que hace cosa de un año movimos de Azure/Windows a Google Compute Platform/Linux. Más [aquí](https://blog.plasticscm.com/2020/05/announcing-new-plastic-cloud2.html).

· Full import con ramas de Perforce a Plastic… y de vuelta. Esto requiere saberse todo de ambos sistemas. También lo hacemos con Git, por cierto.

Y cosas que tenemos por delante:

· Sistema de locks distribuidos. ¿Te suena lo de bloquear ficheros que no se pueden mergear? Vale, ¿cómo llevas eso al mundo distribuido con equipos en diferentes partes del mundo? Es una de las cosas que tenemos que resolver en breve.

· Virtual filesystem para macOS y Linux (tenemos un prototipo, pero le queda mucho).

· Compactación de repositorios con mínimo down time.

Al final es un equipo que hace la base de todo lo que desarrolla el resto, y toca desde base de datos (ahora menos) a nuestro propio almacenamiento basado en [memory mapped files](https://blog.plasticscm.com/2018/06/story-of-jet-fast-repo-storage.html), código de red de alto rendimiento, estamos trabajando con Konrad Kokosa (el del libro de 1000 páginas de .net memory) para reducir allocations y mejorar velocidad, etc, etc.

### Qué te ofrecemos en Unity

Además de los retos técnicos que te decía antes:

· 30 días de vacaciones.

· Compensación MUY competitiva, incluyendo stock.

· Presupuesto para material de oficina para trabajar desde casa (en plan, necesito una pantalla 4k para casa).

· Material de primera (ahora todo el equipo tiene macbook pro 16, de 2TB, 64GB RAM, etc… estamos intentando usar macOS todo lo que podemos para mejorar Plastic ahí).

· Formación.

· Proyección. Un _individual contributor_ (IC) en Unity tiene una proyección enorme. Hay muchos niveles, y puedes subir incluso hasta nivel Vicepresidente siendo desarrollador.

· Trabajar con equipos de todo el mundo. 2 de nuestros equipos están en Seattle, los product managers en Canadá, tenemos gente en Austin (Texas), etc.

### Cómo trabajamos

Una de las cosas que nos definen es que entregamos sin parar. Intentamos no poner excusas sino entregar valor. Si te vas a la página de downloads de plasticscm.com, verás que sacamos una versión a la semana, a veces más.

Llevamos 373 sprints, y aunque ya no usamos Scrum (y no es que no nos guste, es que hemos cambiado cosas), seguimos midiendo el tiempo en sprints, pero no entregamos al final de cada 2 semanas, sino continuamente.

Puedes leer aquí la historia de cómo cambiamos de Scrum a Kanban y como el cycle time se ha convertido en nuestra métrica base: [https://medium.com/@psluaces/scrum-a-kanban-2-veces-mas-rapido-f6c0802d93f1](https://medium.com/@psluaces/scrum-a-kanban-2-veces-mas-rapido-f6c0802d93f1)

También puedes leer más sobre nuestra forma de entender el desarrollo en nuestro libro: [https://www.plasticscm.com/book/#\_2\_principles\_for\_project\_management](https://www.plasticscm.com/book/#_2_principles_for_project_management)

### Qué es Plastic SCM y qué tiene que ver con Unity

En agosto de 2020 [Unity adquirió Códice Software](https://www.xataka.com/empresas-y-economia/unity-adquiere-empresa-espanola-codice-software-a-su-producto-estrella-plastic-scm-alternativa-a-git), una empresa de Boecillo, Valladolid, que desarrolla Plastic SCM. Arrancamos en 2005, con el sueño de crear un control de versiones mejor que Perforce, Subversion, Clearcase… y acabamos compitiendo con Git, que nació el mismo año que nosotros arrancamos.

Así que ahora somos el control de versiones de Unity, y nuestra misión es convertirnos en el mejor sistema de colaboración para creadores de contenido 3D (que es videojuegos pero mucho más, hay fabricantes de coches usando Unity para simulaciones, empresas de arquitectura, y las aplicaciones crecen cada día).

Pero Plastic no es solo para videojuegos. Nuestro cliente más grande, con más de 3mil licencias, es una empresa de automoción, y tenemos de todo, desde un equipo en la NASA, hasta empresas de 3 personas, grupos de más de 1000, y en todos los sectores.
