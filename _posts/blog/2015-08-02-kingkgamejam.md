---
layout: blogarticle-layout
title: Impulsa Game Jams - King K.
comments: true
author: esteban_gaete
categories:
- blog
tags:
- King K
- GameJam
- Post-Mortem
image:
    cover: blog/cover/kk-cover.png
    teaser: blog/teaser/kk-teaser.png
---

<p class="margin-top-30" markdown='1'>
Durante todo el mes de Julio se desarrolló la [Impulsa Games Jams #IG2A43](http://jams.gamejolt.io/codenameig2a43) la cual estuvo basada en el 
aniversario número 43 de Atari, por lo que se debía hacer un juego con apariencia audio/visual similar a alguna de las consolas clásicas de 
Atari. Nosotros elegimos la **Atari 2600** ya que es la más conocida y la más clásica de todas.
</p>

<p class="margin-top-30" markdown='1'>
Adicional a las [condiciones bases de la game jam](http://impulsagames.com/foro/showthread.php?tid=34) nuestra cuchara **Esteban Gaete** decidió auto-imponerse un reto: grabarse programando y no trabajar más de 30 minutos al día en la game jam. ¿Lo habrá logrado?
</p>

<p class="margin-top-30">
    <ul>
        <li>
            <p markdown='1'>
                El juego puede descargarse desde: [Gamejolt - King K. A Goblin Defense Game](http://gamejolt.com/games/king-k-a-goblin-defense-game/82821).
            </p>
        </li>
        <li>
            <p markdown='1'>
                El video Devlog improvisado puede verse desde: [Youtube - Impulsa Game Jams - Devlog Improvisado](https://www.youtube.com/playlist?list=PLsHCX_FQmzl10YF_8m0oxfsLPKwhw7kXb)
            </p>
        </li>
    </ul>
</p>

<p class="margin-top-30" markdown='1'>
A continuación se mostrarán en breve los diferentes avances y los resultados finales del juego:
</p>

<div class="page-header margin-top-30" markdown='1'>
## Desarrollo de la Game Jam
</div>

<p class="margin-top-30" markdown='1'>
El desarrollo propiamente tal comenzó el 10 de Julio y se mantuvo un desarrollo constante de 30 minutos al día casi todos los días. Hubo días en los que no se pudo trabajar y por lo mismo algunas partes duran una hora, ya que considera el tiempo de dos días.
</p>

<p class="margin-top-30" markdown='1'>
Lo primero fue definir el tipo de juego y el escenario. Los videos comenzaron sin tener claro que hacer por lo que durante una rápida lluvia de ideas en la primera parte del vídeo se llegó a la siguiente conclusión:
</p>

<p class="margin-top-30">
    <p align="center"><img src="{{ site.url }}/img/blog/content/goblinmina01-preview.png"></p>
</p>

<p class="margin-top-30" markdown='1'>
La idea en resumen trata sobre: *Un juego similar a un tower defense donde se debe proteger al rey goblin de sucios humanos que quieren acabar con todos, la diferencia es que esta vez será en 2D, se controlará a cinco goblins y se tendrá acceso a una forja donde es posible mejorar ciertas estadísticas y crear trampas*.
</p>

<p class="margin-top-30" markdown='1'>
En conjunto con el mapa se creó un diagrama de clases para la arquitectura del nivel, de forma que se llego a lo siguiente:
</p>

<p class="margin-top-30">
    <p align="center"><img src="{{ site.url }}/img/blog/content/diagramapapayapa01-preview.png"></p>
</p>

<p class="margin-top-30" markdown='1'>
De modo que un nivel se compone de una sección de estadísticas, una GUI para mostrar la estadística, una Forja compuesta de trampas y equipos, y finalmente personajes, que se dividen en humanos y goblins (que a su vez tienen un miembro llamado Rey Goblin). Luego se definieron los gráficos prototipos para el goblin, el goblin rey y los humanos.
</p>

<p class="margin-top-30">
    <p align="center"><img src="{{ site.url }}/img/blog/content/goblin-bocetospj.png"></p>
</p>

<p class="margin-top-30" markdown='1'>
Pero que hermosura de pixeles.
</p>

<p class="margin-top-30" markdown='1'>
Afortunadamente no alcancé a usar estos gráficos en el desarrollo ya que nuestro buen amigo [Don Calaca](http://c1ic.mx/) nos proporcionó estos excelentes gráficos:
</p>

<p class="margin-top-30">
    <p align="center"><img src="{{ site.url }}/img/blog/content/goblingif-preview.gif"></p>
</p>

<p class="margin-top-30" markdown='1'>
El paso siguiente consistió en crear los cinco goblins principales y poder cambiar el control sobre ellos.
</p>

<p class="margin-top-30">
    <p align="center"><img src="{{ site.url }}/img/blog/content/goblingif2-preview.gif"></p>
</p>

<p class="margin-top-30" markdown='1'>
Se usa también una letra S a modo de prueba para marcar cual goblin está siendo seleccionado. A continuación se ingresaron los humanos al escenario y se hicieron pruebas de colisión para poder chocar con el humano y poder atacarlo, todo esto tomó bastante tiempo pero dio buenos resultados.
</p>

<p class="margin-top-30">
    <p align="center"><img src="{{ site.url }}/img/blog/content/goblingif3-preview.gif"></p>
</p>

<p class="margin-top-30">
    <p align="center"><img src="{{ site.url }}/img/blog/content/goblingif4-preview.gif"></p>
</p>

<p class="margin-top-30">
    <p align="center"><img src="{{ site.url }}/img/blog/content/goblingif5-preview.gif"></p>
</p>

<p class="margin-top-30" markdown='1'>
El problema que se hizo evidente al desarrollar esto fue que no es posible determinar si se golpeó realmente al humano, cuánto daño se hizo ni cuanta vida le queda, por ello se hizo un sistema muy simple tipo RPG para mostrar la vida y el daño.
</p>

<p class="margin-top-30">
    <p align="center"><img src="{{ site.url }}/img/blog/content/goblingif6-preview.gif"></p>
</p>

<p class="margin-top-30" markdown='1'>
Con esto solo falta el Rey y...
</p>

<p class="margin-top-30">
    <p align="center"><img src="{{ site.url }}/img/blog/content/goblingif7-preview.gif"></p>
</p>

<p class="margin-top-30" markdown='1'>
La mecánica principal ya está implementada! Los siguientes pasos fue implementar las estadísticas y hacer la forja,
lo primero consistió en acceder a diferentes variables generales del Nivel y globales para luego mostrarlas en textos.
</p>

<p class="margin-top-30">
    <p align="center"><img src="{{ site.url }}/img/blog/content/goblingif9-preview.png"></p>
</p>

<p class="margin-top-30" markdown='1'>
La forja por otra parte consistía de un menú simple con tres opciones que se seleccionaban con enter, si se cumplían los requisitos mínimos se accedía a la bonificación.
</p>

<p class="margin-top-30">
    <p align="center"><img src="{{ site.url }}/img/blog/content/goblin-forja.png"></p>
</p>

<p class="margin-top-30" markdown='1'>
Lo último a trabajar y que se hizo durante los últimos dos días, los únicos días en los que no se pudo trabajar 30 minutos, si no que se trabajaron varias horas debido al poco tiempo que quedaba y al trabajo que aún faltaba hacer, se trabajó el retoque gráfico del juego. Primero se agregaron más iconos como lo visto en la forja:
</p>

<p class="margin-top-30">
    <p align="center"><img src="{{ site.url }}/img/blog/content/goblin-tutorial2.png"></p>
</p>

<p class="margin-top-30" markdown='1'>
Estos fueron usados en el escenario principal, dándole un toque más acabado y decente:
</p>

<p class="margin-top-30">
    <p align="center"><img src="{{ site.url }}/img/blog/content/goblin-fight2.png"></p>
</p>

<p class="margin-top-30" markdown='1'>
Además cabe notar que los goblins pueden subir de nivel cada dos humanos derrotados, de forma que estos aumentan de tamaño y tienen más vida. Finalmente se agregó la música y los efectos especiales, la música puede ser escuchada directamente en la página de gamejolt sin tener que bajar el juego: [Gamejolt - King K. A Goblin Defense Game](http://gamejolt.com/games/king-k-a-goblin-defense-game/82821).
</p>

<p class="margin-top-30" markdown='1'>
Lo último a realizar fue el menú y las imágenes de presentación del juego:
</p>
<p class="margin-top-30">
    <p align="center"><img src="{{ site.url }}/img/blog/content/goblin-portada.gif"></p>
</p>

<p class="margin-top-30" markdown='1'>
Y con esto el juego se dio por finalizado :D Una grata experiencia con Monogame 3.4 y C#, sí, no lo dije antes pero todo esto fue hecho con Monogame, partiendo desde cero.
</p>

<div class="page-header margin-top-30" markdown='1'>
## Resultados Finales
</div>

<p class="margin-top-30" markdown='1'>
En conjunto con el desarrollo del juego se grabó un DevLog improvisado en el que se explica cada avance y cada línea de código escrito.
</p>

<p class="margin-top-30">
    <ul>
        <li>
            <p markdown='1'>
                [Youtube - Impulsa Game Jams - Devlog Improvisado](https://www.youtube.com/playlist?list=PLsHCX_FQmzl10YF_8m0oxfsLPKwhw7kXb)
            </p>
        </li>
    </ul>
</p>

<p class="margin-top-30" markdown='1'>
El juego puede probarse en el siguiente link:
</p>

<p class="margin-top-30">
    <ul>
        <li>
            <p markdown='1'>
                [Gamejolt - King K. A Goblin Defense Game](http://gamejolt.com/games/king-k-a-goblin-defense-game/82821).
            </p>
        </li>
    </ul>
</p>


<p class="margin-top-30" markdown='1'>
Finalmente algunas estadísticas:
</p>

<p class="margin-top-30">
    <ul>
        <li>
            <p>
                Framework y lenguaje usado: Monogame 3.4 con C#.
            </p>
        </li>
        <li>
            <p>
                Días de desarrollo: 21 días.
            </p>
        </li>
        <li>
            <p>
                Horas reales de desarrollo: 1560 minutos, es decir, 26 horas.
            </p>
        </li>
        <li>
            <p>
                Líneas de código: 1473.
            </p>
        </li>
        <li>
            <p>
                Clases creadas: 19.
            </p>
        </li>
        <li>
            <p>
                Auto-desafío de 30 minutos al día: Cumplido a excepción de los dos últimos días.
            </p>
        </li>
    </ul>
</p>



<div class="page-header margin-top-30" markdown='1'>
## Conclusión
</div>

<p class="margin-top-30" markdown='1'>
Programar es divertido! Jajá. La conclusión es que hay que siempre tener cuidado con las metas que uno se plantea en un tiempo dado, había mucho más que quería hacer, y si bien logré hacer la mayoría de las cosas el hecho de que no haya alcanzado a hacer tal cual lo que deseaba es producto de que aún tengo problemas para estimar bien mi tiempo.
</p>

<p class="margin-top-30" markdown='1'>
Espero poder participar en más GameJam (de hecho ya tengo dos más en la mira) y poder hacer más análisis y videos como este.
</p>
