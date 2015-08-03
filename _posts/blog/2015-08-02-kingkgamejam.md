---
layout: article
title: Impulsa Game Jams - King K.
comments: true
author: esteban_gaete
categories:
- blog
tags:
- King K
- GameJam
image:
    feature: featured/kk-featured.png
    teaser: teaser/kk-teaser.png
summary: Game Jam con gráficos de Atari 2600 y desafíos auto-implementados. ¿Se habrá logrado el reto?
---

Durante todo el mes de Julio se desarrolló la [Impulsa Games Jams #IG2A43](http://jams.gamejolt.io/codenameig2a43) la cual estuvo basada en el 
aniversario número 43 de Atari, por lo que se debía hacer un juego con apariencia audio/visual similar a alguna de las consolas clásicas de 
Atari. Nosotros elegimos la **Atari 2600** ya que es la más conocida y la más clásica de todas.

Adicional a las [condiciones bases de la game jam](http://impulsagames.com/foro/showthread.php?tid=34) nuestra cuchara **Esteban Gaete** decidió auto-imponerse un reto: grabarse programando y no trabajar más de 30 minutos al día en la game jam. ¿Lo habrá logrado?

* El juego puede descargarse desde: [Gamejolt - King K. A Goblin Defense Game](http://gamejolt.com/games/king-k-a-goblin-defense-game/82821).
* El video Devlog improvisado puede verse desde: [Youtube - Impulsa Game Jams - Devlog Improvisado](https://www.youtube.com/playlist?list=PLsHCX_FQmzl10YF_8m0oxfsLPKwhw7kXb)

A continuación se mostrarán en breve los diferentes avances y los resultados finales del juego:

## Desarrollo de la Game Jam

El desarrollo propiamente tal comenzó el 10 de Julio y se mantuvo un desarrollo constante de 30 minutos al día casi todos los días. Hubo días en los que no se pudo trabajar y por lo mismo algunas partes duran una hora, ya que considera el tiempo de dos días.

Lo primero fue definir el tipo de juego y el escenario. Los videos comenzaron sin tener claro que hacer por lo que durante una rápida lluvia de ideas en la primera parte del vídeo se llegó a la siguiente conclusión:

<p align="center"><img src="http://www.spoonmangames.cl/images/preview/mina01-preview.png"></p>

La idea en resumen trata sobre: *Un juego similar a un tower defense donde se debe proteger al rey goblin de sucios humanos que quieren acabar con todos, la diferencia es que esta vez será en 2D, se controlará a cinco goblins y se tendrá acceso a una forja donde es posible mejorar ciertas estadísticas y crear trampas*.

En conjunto con el mapa se creó un diagrama de clases para la arquitectura del nivel, de forma que se llego a lo siguiente:

<p align="center"><img src="http://www.spoonmangames.cl/images/preview/diagramapapayapa01-preview.png"></p>

De modo que un nivel se compone de una sección de estadísticas, una GUI para mostrar la estadística, una Forja compuesta de trampas y equipos, y finalmente personajes, que se dividen en humanos y goblins (que a su vez tienen un miembro llamado Rey Goblin). Luego se definieron los gráficos prototipos para el goblin, el goblin rey y los humanos.

<p align="center"><img src="http://www.spoonmangames.cl/images/preview/goblin-bocetospj.png"></p>

Pero que hermosura de pixeles.

Afortunadamente no alcancé a usar estos gráficos en el desarrollo ya que nuestro buen amigo [Don Calaca](http://c1ic.mx/) nos proporcionó estos excelentes gráficos:

<p align="center"><img src="http://www.spoonmangames.cl/images/preview/goblingif-preview.gif"></p>

El paso siguiente consistió en crear los cinco goblins principales y poder cambiar el control sobre ellos.

<p align="center"><img src="http://www.spoonmangames.cl/images/preview/goblingif2-preview.gif"></p>

Se usa también una letra S a modo de prueba para marcar cual goblin está siendo seleccionado. A continuación se ingresaron los humanos al escenario y se hicieron pruebas de colisión para poder chocar con el humano y poder atacarlo, todo esto tomó bastante tiempo pero dio buenos resultados.

<p align="center"><img src="http://www.spoonmangames.cl/images/preview/goblingif3-preview.gif"></p>

<p align="center"><img src="http://www.spoonmangames.cl/images/preview/goblingif4-preview.gif"></p>

<p align="center"><img src="http://www.spoonmangames.cl/images/preview/goblingif5-preview.gif"></p>

El problema que se hizo evidente al desarrollar esto fue que no es posible determinar si se golpeó realmente al humano, cuánto daño se hizo ni cuanta vida le queda, por ello se hizo un sistema muy simple tipo RPG para mostrar la vida y el daño.

<p align="center"><img src="http://www.spoonmangames.cl/images/preview/goblingif6-preview.gif"></p>

Con esto solo falta el Rey y...

<p align="center"><img src="http://www.spoonmangames.cl/images/preview/goblingif7-preview.gif"></p>

La mecánica principal ya está implementada! Los siguientes pasos fue implementar las estadísticas y hacer la forja,
lo primero consistió en acceder a diferentes variables generales del Nivel y globales para luego mostrarlas en textos.

<p align="center"><img src="http://www.spoonmangames.cl/images/preview/goblingif9-preview.png"></p>

La forja por otra parte consistía de un menú simple con tres opciones que se seleccionaban con enter, si se cumplían los requisitos mínimos se accedía a la bonificación.

<p align="center"><img src="http://www.spoonmangames.cl/images/preview/goblin-forja.png"></p>

Lo último a trabajar y que se hizo durante los últimos dos días, los únicos días en los que no se pudo trabajar 30 minutos, si no que se trabajaron varias horas debido al poco tiempo
que quedaba y al trabajo que aún faltaba hacer, se trabajó el retoque gráfico del juego. Primero se agregaron más iconos como lo visto en la forja:

<p align="center"><img src="http://www.spoonmangames.cl/images/preview/goblin-tutorial2.png"></p>

Estos fueron usados en el escenario principal, dándole un toque más acabado y decente:

<p align="center"><img src="http://www.spoonmangames.cl/images/preview/goblin-fight2.png"></p>

Además cabe notar que los goblins pueden subir de nivel cada dos humanos derrotados, de forma que estos aumentan de tamaño y tienen más vida. Finalmente se agregó la música y los efectos especiales,
la música puede ser escuchada directamente en la página de gamejolt sin tener que bajar el juego: [Gamejolt - King K. A Goblin Defense Game](http://gamejolt.com/games/king-k-a-goblin-defense-game/82821).

Lo último a realizar fue el menú y las imágenes de presentación del juego:

<p align="center"><img src="http://www.spoonmangames.cl/images/preview/goblin-portada.gif"></p>

Y con esto el juego se dio por finalizado :D Una grata experiencia con Monogame 3.4 y C#, sí, no lo dije antes pero todo esto fue hecho con Monogame, partiendo desde cero.

## Resultados Finales

En conjunto con el desarrollo del juego se grabó un DevLog improvisado en el que se explica cada avance y cada línea de código escrito.

* [Youtube - Impulsa Game Jams - Devlog Improvisado](https://www.youtube.com/playlist?list=PLsHCX_FQmzl10YF_8m0oxfsLPKwhw7kXb)

El juego puede probarse en el siguiente link:

* [Gamejolt - King K. A Goblin Defense Game](http://gamejolt.com/games/king-k-a-goblin-defense-game/82821).

Finalmente algunas estadísticas:

* Framework y lenguaje usado: Monogame 3.4 con C#.
* Días de desarrollo: 21 días.
* Horas reales de desarrollo: 1560 minutos, es decir, 26 horas.
* Líneas de código: 1473.
* Clases creadas: 19.
* Auto-desafío de 30 minutos al día: Cumplido a excepción de los dos últimos días.

## Conclusión

Programar es divertido! Jajá. La conclusión es que hay que siempre tener cuidado con las metas que uno se plantea en un tiempo dado, había mucho más que quería hacer, y si bien logré hacer la mayoría de las cosas el hecho de que no haya alcanzado a hacer tal cual lo que deseaba es producto de que aún tengo problemas para estimar bien mi tiempo.

Espero poder participar en más GameJam (de hecho ya tengo dos más en la mira) y poder hacer más análisis y videos como este.

