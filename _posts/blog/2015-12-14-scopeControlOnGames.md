---
layout: blogarticle-layout
title: Manejando el Tamaño de un vídeojuego
comments: true
author: esteban_gaete
categories:
- blog
tags:
- Blog
image:
    teaser: blog/teaser/scopeControl-teaser.gif
    cover: blog/cover/scopeControl-cover.png
    featured: blog/featured/scopeControl-featured.png
    featured-text: Tablero de tareas de Descend Into Heaven.
---

<p class="margin-top-30">
A quién no le ha pasado que te llenas de ideas pensando sobre cómo hacer tu juego, cuáles serán todas las mecánicas, los niveles, la historia, los personajes, etc y etc! Todos en esta industria somos tan apasionado con lo que hacemos que es fácil dejarnos llevar por esto, terminando con un concepto de juego tan grande y ambicioso que fácilmente podría considerarse un juego triple A de gran presupuesto, un amplio equipo de desarrollo y extenso periodo de producción.
</p>

<p class="margin-top-30" markdown='1'>
Si somos sinceros la verdad es que es muy difícil realizar un juego de esa envergadura en la escena Indie, la gran mayoría de las **empresas independientes de desarrollo de vídeojuegos** cuentan con un equipo de entre 2 a 5 personas, un presupuesto muy apretado que suele depender de otros proyectos y poco tiempo para dedicarse con exclusividad a trabajar en un juego propio. Esto nos deja con muy pocas opciones, trabajar años y años en un tu juego, gastando muchas horas de sueño y de vida personal, atrapado en un ciclo de producción eterno, que **en vez de irse acabando va creciendo** con cada idea nueva que se nos ocurre.
</p>

<p class="margin-top-30" markdown='1'>
Ha ocurrido millones de veces en la industria y es uno de los factores principales por lo que las empresas se van a la quiebra y cierran, ya sea porque no hay suficiente presupuesto para seguir desarrollando el juego, o bien, **el juego salió a la venta y no vendió tan bien** como para recuperar toda la inversión hecha durante todos estos años. Si miras algunos juegos que han pasado por esto y ves entrevistas al respecto te darás cuenta que ninguno de los directores quiere hacer algo así nuevamente, “aprender a planificar” es la lección número uno que siempre predican después de tan infernal experiencia y es que nadie tiene el respaldo (económico y popular) como para estar 5 o 7 años desarrollando un juego cómo Blizzard con Stracraft II y salir con cifras positivas. *Si estás interesado en este tipo de historias al final del documento dejaré una lista de links con temas relacionados para que enriquezcas tu lectura*.
</p>

<p class="margin-top-30" markdown='1'>
Me imagino que se estarán preguntando, *“¿Y a que va todo esto querido **Spoonman**?”*, pues queridos lectores, en **Spoonman Games** hemos tenido malas, muy malas y también algunas buenas experiencias respecto al manejo del tamaño (también conocido como alcance o scope en inglés)  de proyectos de desarrollo de software, por lo que esta entrada tratará sobre algunos trucos que hemos aprendido en el camino así como las técnicas comunes usadas en este tipo de proyectos. Es posible que esto no aplique a todo tipo de juegos, pero espero que te ayude a tener una guía en tu desarrollo. *Si prefieres no leer todo el blog explicativo y saltar directamente a una lista resumen haz [click aquí](#resumen)*.
</p>

<div class="page-header margin-top-30" markdown='1'>
## Experiencia
</div>

<p class="margin-top-30" markdown='1'>
Como les venía contando, en **Spoonman Games** tenemos un poco de experiencia con este tema, nuestra cuchara **Victor Gaete** ya lleva más de 7 años en el mundo del desarrollo de software empresarial y por otro lado está la cuchara **Esteban Gaete**, quién desde el 2010 ha intentado formar esta empresa (pueden leer un poco de eso aquí) y que desde entonces ha estado trabajando en distintos desarrollo de software, tanto empresariales como vídeojuegos. Sin embargo en cuanto a lo que es **Spoonman Games** podemos presumir de lo siguiente:
</p>

 * <p class="margin-top-30" markdown='1'>Win 10 Game Jam (Marzo 2015): Tercer lugar con [Sunset Roboto: The Eternal Rider](http://www.spoonmangames.cl/blog/win10gamejam/), tiempo 24 horas.</p>
 * <p markdown='1'>Impulsa Game Jam (Julio 2015): Duró un mes, se creó [King K. A goblin defense game](http://www.spoonmangames.cl/blog/kingkgamejam/) trabajando 30 minutos al día.</p>
 * <p markdown='1'>GBJAM 4 (Agosto 2015): Creado [Descend Into Heaven](http://www.spoonmangames.cl/blog/timelapsedih/) en 5 días, luego el juego se expandió y mejoro considerablemente en un tiempo de dos meses.</p>

<p class="margin-top-30" markdown='1'> 
Como podrán ver los tiempos de desarrollo son bastante cortos, en particular *Descend Into Heaven*, que es un juego bastante largo, fue desarrollado sin problemas ni contingencias de último minuto. En estos momentos también nos encontramos trabajando en *Tower of Horizon*, juego que planea salir a finales de Enero en toda su gloria.
</p>

<p class="margin-top-30" markdown='1'>
¿Cuál es el truco?
</p>

<div class="page-header margin-top-30" markdown='1'>
## La piedra angular
</div>

<p class="margin-top-30" markdown='1'>
Cuando deseas crear tu juego y estás en el proceso creativo de ver todo lo que quieres hacer, sé libre, sueña y visualiza tu juego perfecto, no hay límites hasta que tan lejos puedes llegar!, pero hazlo una sola vez, piénsalo muy bien y tomate un buen tiempo antes de comenzar a desarrollar, pueden ser unos días o una semana, has prototipos en papel, dibujos y hasta diagramas, pero hazlo todo antes de comenzar el desarrollo del juego. Esto no quiere decir que si piensas “tendré un mundo de nieve en mi juego” que tendrás que hacer el diseño del nivel, los enemigos o jefes, lo que quiere decir es que considerarás dentro de tu desarrollo, tanto en cuanto a tiempo y a esfuerzo, la posibilidad de hacer un mundo de nieve. Básicamente este proceso se puede resumir como un **GDD muy simplificado** de lo que es tu juego (para leer sobre lo que es un GDD has [click aquí](http://www.spoonmangames.cl/blog/gddOverview/)).
</p>

<p class="margin-top-30" markdown='1'>
Ahora, el GDD simplificado es la parte fácil, ya que una vez terminado el documento tienes que contrastarlo con el requerimiento número 1: **el tiempo**. Si eres una persona seria en el desarrollo y haces esto como negocio entonces debes tener un tiempo de inicio y de fin para el desarrollo de tu juego, esto se puede dividir en dos escenarios.
</p>

 * <p class="margin-top-30">Deadline: Tiempo límite máximo no modificable y crítico. Normalmente presentes en Game Jams, Hackatón o maratones de programación, así como también cuando se trabaja para un cliente o Publisher.</p>
 * <p>Softline: Tiempo límite máximo parcialmente modificable y no del todo crítico. Normalmente presentes cuando el juego es desarrollado y financiado de forma propia o mediantes programas de financiamiento.</p>

<p class="margin-top-30" markdown='1'>
Eventualmente, sea cuál sea el caso, el objetivo debe ser cumplir con la fecha y no hacer modificaciones, así que es hora de la practica favorita de todos: **estimar el tiempo!** Yay… *no les gusta?* Pues no es algo muy bien visto, a pesar de que es una práctica muy usada  es imposible estimar con exactitud y lo que uno termina haciendo es calzar todas tus ideas en ese tiempo, hacer todo a media y terminar con un juego poco claro.
</p>

<p class="margin-top-30" markdown='1'>
Entonces, ¿cuál es la idea? ¿Recuerdas tu **GDD muy simplificado?** Es hora de limarlo y ordenarlo. Debes detectar cuales son las funcionalidades claves de tu juego y luego ordenar éstas en prioridad de desarrollo, siendo la más importante la primera que se hará. Lo natural a detectar en este punto es el gameplay, si por ejemplo tu juego es un plataformer, primero has que el personaje se mueva, salte, ataque, muera, vuele, se transforme, colisiones, etc, dependiendo lo que quieras hacer. Estas funcionalidades deben quedar listas y muy pulidas al comienzo, aquí tanto el programador, como el animador/diseñador gráfico y el diseñador de sonidos pueden trabajar en paralelo para crear todo lo necesario. Vuelvo a destacar que son los **aspectos más importantes**, es decir, si tu personaje usará armas y tendrá una variedad muy grande de ellas tu objetivo en esta parte es hacer el arma principal solamente, ni más ni menos, lo mismo aplicado a otras características. Es decir, debes desarrollar la esencia, la piedra angular de tu juego y sin irte por las ramas.
</p>

<p class="margin-top-30" markdown='1'>
Una vez que hayas terminado con este proceso es importante que hagas un prototipo donde puedas probar estos aspectos esenciales y ver que funcionan correctamente. Esto debe ser rápido y dependiendo el tipo de juego puede tomar desde un día hasta un par de semanas considerando que trabajas en él todos los días.
</p>

<p class="margin-top-30" markdown='1'>
*“Todo va muy bien **Spoonman**, pero el GDD simplificado está lleno de ideas y no hemos hecho nada para manejar el tamaño del juego”*, tienes razón y justamente ahora se viene eso, la parte más divertida.
</p>


<div class="page-header margin-top-30" markdown='1'>
## Los últimos serán los primeros
</div>

<p class="margin-top-30" markdown='1'>
Si has llegado a este punto y has hecho lo que hemos escrito anteriormente, ¡felicidades! Cuentas con un juego que en esencia es lo que tú quieres que sea y que puede llegar a ser cualquier cosa según como lo guíes.
</p>

<p class="margin-top-30" markdown='1'>
Una de las técnicas que hemos estado desarrollando y aplicando en **Spoonman Games** es lo que sugiere el título de esta sección: *Los últimos serán los primeros*. Y esto es literal.
</p>

<p class="margin-top-30" markdown='1'>
Comienza desarrollando la batalla final de tu juego y el nivel final del juego que tiene en mente, y sí, debes estar pensando que es una locura o que es imposible, no has pensado ni la cantidad de niveles ni el sistema de experiencia, ni la selección de niveles, ni el menú del juego, ni … detente ahí. Es cierto, hay muchas cosas que parecieran ser más importantes y que debieran hacerse antes, porque ese es el orden en el que tú sueles JUGAR los juegos, pero eso no significa que ese sea el orden ideal para desarrollarlos. El objetivo de esto es hacer el juego desde lo más difícil y complejo hasta lo más fácil y trivial. En tu GDD debes tener un listado de niveles que te gustaría hacer, ordénalos según cómo quieres que se jueguen y comienza a desarrollar el último primero, el jugador debiera tener mucha experiencia al jugar estos niveles por lo que puedes hacer desafíos bastante complejos, podrás ver que tan bien funciona la esencia de tu juego y el gameplay, después de todo, si el mundo más complejo y con el boss más difícil es posible jugar y divertirse el resto del juego será igual o mucho mejor.
</p>

<p class="margin-top-30" markdown='1'>
Luego que termines el último escenario de juego avanza hacia el penúltimo, y así, siendo el primer nivel de tu juego el último en desarrollarse. Esto tiene dos grandes ventajas:
</p>

 * <p class="margin-top-30">Para cuando llegues al primer nivel sabrás muy bien como diseñar niveles para tu juego, lo que te permitirá tener un excelente primer nivel introductorio.</p>
 * <p>Durante el desarrollo de los niveles más complicados podrás decidir correctamente si vale la pena implementar esa idea que pensaste en el GDD o si es mejor dejarla de lado.</p>
 * <p>Tendrás un mayor control sobre la experiencia del usuario durante todo el desarrollo del juego.</p>

<p class="margin-top-30" markdown='1'>
Naturalmente mientras trabajas en el diseño de niveles, los gráficos asociados, la música y audio de un nivel irás dándote cuenta de la prioridad de otras tareas, y de a poco comenzarás a desarrollar menús, selección de niveles, tipos de armas, tipos de enemigos, tipos de jefes, etc.
</p>

<p class="margin-top-30" markdown='1'>
Puede que pienses que en realidad hacer el primer nivel es sumamente importante, si ese es el caso te recomiendo hacer el último y el primer nivel, y luego hacer los niveles intermedios. La principal razón de porque hacer el nivel final sí o sí es por algo que ya mencioné un poco más atrás: **el tiempo**.
</p>

<p class="margin-top-30" markdown='1'>
Mientras más te acerques a la fecha final de salida de tu juego comenzarás a ver cuánto de tu GDD puedes hacer en el tiempo que te queda, por lo que puedes cortar contenido, sacar niveles y unir todo lo que has hecho hasta entonces para formar el juego, pero como partiste desde el último nivel hasta el primero, te darás cuenta que, aunque has sacado contenido, **lo más interesante y divertido de tu juego estará presente junto con la experiencia que quieres transmitir**, permitiéndote, aunque tu juego sea demasiado ambicioso, tener un juego completo, conciso y coherente que todos podrán jugar y disfrutar.
</p>

<p class="margin-top-30" markdown='1'>
Podría seguir hablando de este punto y de muchos más para ayudarte a controlar el tamaño de tu juego, pero este blog se volvería muy largo, así que te invito a ver los dos siguientes videos sobre nuestros juegos *King K. A Goblin Defense Game* y *Descend Into Heaven*, vídeos en los cuales hablamos sobre el desarrollo y este tipo de estrategias. Y si te gustaría que escribiera **un artículo más detallado al respecto**, déjanos saber en la sección de comentarios!
</p>

<div class="embed-video-container embed-responsive embed-responsive-16by9 margin-top-30">
    <iframe src="https://www.youtube.com/embed/PUiRDrq3Ux8" class="embed-responsive-item"></iframe>
</div>

<div class="embed-video-container embed-responsive embed-responsive-16by9 margin-top-30">
    <iframe src="https://www.youtube.com/embed/lbodT_K15TU" class="embed-responsive-item"></iframe>
</div>

<div class="page-header margin-top-30">
    <h2 id="resumen">Resumen y conclusión</h2>
</div>

<p class="margin-top-30" markdown='1'>
En resumen está es la estrategia para mantener en control el tamaño de tu juego:
</p>

 * <p class="margin-top-30">Desarrollar un GDD muy simplificado con todas las ideas que se te ocurran sobre tu juego.</p>
 * <p>El proceso de creación e inclusión de ideas solo se da fuertemente al comienzo y se debe evitar más adelante.</p>
 * <p>Fijar la fecha de inicio y término del proyecto.</p>
 * <p>Identificar los aspectos más importantes de tu juego, en cuanto a gameplay y su concepto.</p>
 * <p>Ordenar por prioridad los aspectos más importantes encontrados.</p>
 * <p>Implementar la base de estos aspectos hasta estar satisfecho.</p>
 * <p>Ordenar el flujo de tu juego (niveles, mundos, secuencias, etc) según cómo quieres que se juegue.</p>
 * <p>Desarrollar el flujo desde el final hacia adelante.</p>
 * <p>Detectar cuales ideas de verdad valían la pena.</p>
 * <p>Cortar el desarrollo al estar cerca de la fecha final para armar el juego y darle coherencia.</p>

<p class="margin-top-30" markdown='1'>
Está estrategia nos ha sido muy útil tanto en desarrollo de juegos personales como en Game Jams, has la prueba y verás que funciona de maravilla. Aunque no lo parezca a primera vista este modelo te ofrece mucha libertar de experimentación y te permite caracterizar rápidamente el juego con tu idea, además de también ofrecer gran resistencia al cambio y a los riesgos que salgan en el camino, ya que una vez que has hecho un par de niveles o mundos el desarrollo del juego puede terminarse en cualquier momento y el resultado será un juego bastante completo y jugable.
</p>

<p class="margin-top-30" markdown='1'>
En **Spoonman Games** no hemos tenido la oportunidad de probar esto con todo tipo de juegos, por lo que es altamente probable que con algunos estilos no sea muy aplicable (por ejemplo en Aventuras gráficas), pero aun así creo que vale la pena intentarlo. Espero les haya sido útil esta lectura y que hayan aprendido algo o se les haya ocurrido algo mejor! Comparte con nosotros tus ideas y mantengamos la discusión activa para mejorar estas técnicas y que en un futuro podamos olvidarnos de lo que es el **Development Hell**.
</p>

<p class="margin-top-30">
Saludos ~
</p>

<div class="page-header margin-top-30" markdown='1'>
## Enriquece tu lectura
</div>

<p class="margin-top-30" markdown='1'>
**Contenido en inglés.**
</p>

 * <p class="margin-top-30" markdown='1'>
    [Development Hell](https://en.wikipedia.org/wiki/Development_hell)
   </p>
 * <p markdown='1'>
    [How long does it take to make an Indie Game](http://www.gamasutra.com/blogs/JosephMirabello/20140407/214931/How_Long_Does_It_Take_to_Make_an_Indie_Game.php)
   </p>
 * <p markdown='1'>
    [Game Development for the Damned and Delirious](http://www.escapistmagazine.com/articles/view/video-games/issues/issue_232/6902-Game-Development-for-the-Damned-and-Delirious)
   </p>
 * <p markdown='1'>
    [Game Developers work such insane hours](http://kotaku.com/crunch-time-why-game-developers-work-such-insane-hours-1704744577)
   </p>
 * <p markdown='1'>
    [How to Scope your game](http://ansimuz.com/site/archives/579)
   </p>
 * <p markdown='1'>
    [How to control Scope in your Project?](http://www.pmexamsmartnotes.com/control-scope-process/)
   </p>
 * <p markdown='1'>
    [How to Manage Scope Creep - and Even prevent it from happening](http://www.liquidplanner.com/blog/manage-scope-creep-even-prevent-happening/)
   </p>
 * <p markdown='1'>
    [Development Hell: The Video Game - The Magic Circle](http://www.polygon.com/features/2014/8/20/6031917/the-magic-circle-jordan-thomas)
   </p>
 * <p markdown='1'>
    [Starcraft II - Post Mortem](http://www.gamespot.com/videos/starcraft-ii-postmortem-interview-with-kaeo-milker/2300-6271953/)
   </p>
 * <p markdown='1'>
    [Speeding up indie game development: a Post Mortem with Long Nguyen](http://robertwhat.com/2013/07/11/speeding-up-indie-game-development-a-postmortem-with-long-nguyen/)
   </p>
 * <p markdown='1'>
    [Scope: A Lesson in Game Design](http://www.gamecareerguide.com/features/508/scope_a_lesson_in_game_design.php)
   </p>
 * <p markdown='1'>
    [Making Your First Game: Minimum Viable Product - Scope Small, Start Right - Extra Credits](https://www.youtube.com/watch?v=UvCri1tqIxQ)
   </p>

