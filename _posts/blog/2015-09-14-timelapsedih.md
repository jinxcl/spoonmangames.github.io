---
layout: article
title: Time Lapse del Desarrollo de Descend Into Heaven
comments: true
author: esteban_gaete
categories:
- blog
tags:
- DIH
- GameJam
- TimeLapse
- PostMortem
image:
    teaser: teaser/dih-teaser.png
summary: Post-mortem de nuestro primero juego en Unity.
---

¡Hola!, bienvenido a este Post-Mortem (con Time-Lapse incluido) de **Descend Into Heaven**, nuestro primer juego utilizando el famoso game engine llamado Unity3D. Este juego nació por dos motivos principalmente: 

* Entre el 8 y el 18 de agosto del 2015 se desarrolló la [GameBoy Jam 4](http://jams.gamejolt.io/gbjam4), que consistía en crear un juego con el Look & Feel de los juegos retro de GameBoy, cumpliendo con todas las limitaciones técnicas que esta consola portátil implicaba.
* Nuestro antiguó y desaparecido miembro *Nikolai* volvió a Spoonman Games! Así que ¿por qué no celebrar su retorno haciendo un nuevo vídeo juego?

Por desgracia nos enteramos algo tarde sobre la GameJam, específicamente el día 13 de agosto, lo que nos dejó con tan solo 5 días para desarrollar nuestro juego. Pasamos por varios problemas usando Unity, pero gracias a esta rica experiencia ahora nos sentimos capaz de hacer lo que sea. Sin embargo, ¿de qué sirve ganar experiencia si está no se comparte? es por ello que a continuación les mostraremos como desarrollamos este juego, paso a paso y que es lo mejor que sacamos de todo esto.

En los siguientes links puedes jugar nuestro juego mientras realizas esta lectura.

* [Gamejolt - Descend Into Heaven](http://gamejolt.com/games/descend-into-heaven/87079).
* [Itch - Descend Into Heaven](http://spoonmangames.itch.io/descendintoheaven)

O si prefieres ver un vídeo tipo Time-Lapse puedes disfrutarlo haciendo click acá abajo!

[VIDEO]

## Origen del Concepto

Lo que nos atrajo de esta Game Jam es que era de corto tiempo y con limitaciones específicas, por lo que decidimos aprovechar la oportunidad para aprender a trabajar con Unity y ver qué tipo de herramientas y diferencias nos entrega respecto a *Monogame*.

Esta vez el equipo no consistió de una sola persona, sino que de dos:

* Nikolai Heríquez se encargaría del diseño de la música y los gráficos.
* Esteban Gaete se encargaría de la programación y el diseño del juego.
* El level design fue trabajado por ambos, así como también el concepto del juego.

Lo primero a definir es como sería, como teníamos poco tiempo este debía ser simple, rápido de trabajar y duradero al jugar, por ello se decidió por un clásico plataformer 2D enfocado en saltar obstáculos y eliminar enemigos, se tendría que pasar una serie de niveles y derrotar a un jefe final. Sin embargo es fácil que un juego de estás características se extienda de sobremanera, que se le agregue demasiado contenido y que nunca se logren concretar las fases finales para terminarlo, así que considerando el poco tiempo que teníamos llegamos a la siguiente conclusión: **hacer el juego desde el final hasta el comienzo**.

## Los últimos serán los primeros

Naturalmente lo primero que hicimos fue crear un pequeño e improvisado diseño arquitectural de las clases principales de una escena, que como ya habrán visto en [King K](http://www.spoonmangames.cl/blog/kingkgamejam/) es muy útil a la hora de programar. El diagrama en cuestión es el siguiente:

<p align="center"><img src="http://www.spoonmangames.cl/images/timelapses/DIH/Arquitectura.JPG"></p>

Luego, creamos la batalla con el jefe final, para ello necesitábamos tener el sprite map del personaje principal, el del boss y el del escenario donde la pelea ocurriría. Nikolai no es diseñador gráfico, por lo que siguiendo sus instintos y dedicándole mucho tiempo logro dar con los siguientes sprites.

<p align="center"><img src="http://www.spoonmangames.cl/images/timelapses/DIH/prota-boss-show.gif"></p>

El desarrollo comenzó cuando estás animaciones estuvieron lista, el primer desafío con Unity fue aprender a usar el Sprite Editor, que si bien no es complicado, el elegir mal un pivote y asignar mal el tamaño de los sprites puede hacer que el desarrollo sea muy muy lento, esto nos consumió grandes cantidades de horas, pero por suerte aprendimos la lección y ahora no nos cuesta nada hacerlo.

A continuación vino el scripting, C# no es un desafió para nosotros ya que llevamos años usándolos en proyectos de distintas categorías, así que el esfuerzo fue en entender cómo funciona el workflow de Unity. Por suerte es muy similar a lo que hace *Monogame*, por lo que en cosas de horas ya teníamos un personaje totalmente funcional moviéndose, atacando y saltando por la pantalla. Además, gracias a las bondades de Unity, implementar un sistema de colisiones nunca había sido tan simple, un par de click y validaciones y ya teníamos un juego en buenas condiciones corriendo.

Con esto ya era posible empezar el diseño de la pelea del boss, primero hice varios bocetos de las fases en un cuaderno, para luego ver cuales valdría la pena implementar o no:

<p align="center"><img src="http://www.spoonmangames.cl/images/timelapses/DIH/bossfight1.png"></p>
<br>
<p align="center"><img src="http://www.spoonmangames.cl/images/timelapses/DIH/Boss4.JPG"></p>

Una vez decidido que fases hacer se creó un escenario de prueba para implementar las funcionalidades básicas del personaje principal, una vez terminado eso se armó el escenario real donde se pelearía con el boss. En este proceso aprendimos mucho sobre máquinas de estados, layers, eventos y cómo manejar el estado del juego desde script generales. Fue la parte más fuerte en programación que tuvimos y la verdad es que fue una buena decisión hacerlo al principio sin la presión del tiempo.

Mientras yo terminaba la pelea del boss Nikolai comenzó la creación de niveles, en particular con el nivel justo antes del boss. En ciertas ocasiones él me hacía pedidos como "impleméntame unos pinchos que maten al protagonista" o "crea una transición de pantallas para poder avanzar" o "crea unos portales para ir a otra escena", etc. Por lo que cuando la pelea del boss ya estuvo totalmente terminada el nivel desarrollado por Nikolai, así como algunas mecánicas básicas del juego también lo estuvieron.

<p align="center"><img src="http://www.spoonmangames.cl/images/timelapses/DIH/scene3-bossfight.png"></p>

El siguiente paso a avanzar fue el de crear un sprite para los enemigos y buscar la forma de mostrar los colores para que se viera como una gameboy. Lo primero fue relativamente fácil y está fue la grandiosa creación de nuestro improvisado artista:

<p align="center"><img src="http://www.spoonmangames.cl/images/timelapses/DIH/badguy-walking.gif"></p>

Sin embargo lo segundo... al principio no se veía muy bien ya que todo lo que hicimos fue cambiar el tinte de cada sprite, a mano. Por lo que como pueden ver no quedó exactamente bien:

<p align="center"><img src="http://www.spoonmangames.cl/images/timelapses/DIH/tinte-rojo.png"></p>

Sin embargo continuamos e implementamos al enemigo principal llamado BadGuy, vimos su comportamiento y modos de ataque, de tal forma que luego lo pudimos implementar en cualquier parte del juego. Con esto Nikolai podía seguir desarrollando niveles con más variedad y yo podía continuar afinando la pelea final del boss. En esta etapa se hicieron varios beta testing para ver cómo era el flujo del juego, pasar de un nivel a otro y ver la dificultad y la diversión que esto entregaba.

Ya que Nikolai luego pasó a diseñar otro nivel yo pasé a diseñar el menú principal del juego. Esto fue muy directo gracias al control de GameObjects y Sprites que Unity ofrece, así que obtuvimos el resultado deseado en pocos minutos.

<p align="center"><img src="http://www.spoonmangames.cl/images/timelapses/DIH/menu.png"></p>

De este punto en adelante se comenzaron a arreglar diversos detalles técnicos y gráficos respecto a la posición de algunos elementos, la velocidad de algunas animaciones, los colores que el escenario tendría, como se harían las transiciones y como se pasaría de un cuadrante a otro.

Fue en este proceso iterativo de ensayo y error que navegando la web descubrí un excelente shader para transformar todo a colores similares a los de gameboy. Esto produjo un grandísimo cambio en como las cosas se veían, mejorando inmediatamente la calidad del juego. El problema fue que tuve que cambiar todos los sprites que tenían tintes a mano a sus colores originales, tomó mucho tiempo, pero finalmente el resultado fue perfecto.

<p align="center"><img src="http://www.spoonmangames.cl/images/timelapses/DIH/shader.png"></p>

La recta final del juego (justo el día antes) consistió en crear transiciones de pixeles que permitieran darle un efecto agradable al juego cuando se pasaba de un estado a otro, de forma que una vez creadas las usamos en todos los momentos claves. Luego agregamos la música (que durante este tiempo Nikolai había estado componiendo) y los efectos especiales de sonido.

Alcanzamos a subir el juego unos pocos minutos antes de que la GameJam acabara, en una carrera para crear la animación final de los créditos del juego.

<p align="center"><img src="http://www.spoonmangames.cl/images/timelapses/DIH/creditos.png"></p>

Si alguno de ustedes asistió a la GameDev Santiago 7, habrá notado que teníamos tres niveles en vez de dos como acá les he contado, esto es porque un día antes de la GameDev 7 creamos un nuevo nivel basado en un diseño que tenía anotado en el cuaderno:

<p align="center"><img src="http://www.spoonmangames.cl/images/timelapses/DIH/LevelDesign1.JPG"></p>

También incluimos varias mejoras que ahora mismo pueden probar en el juego. Hay mucho que aún tenemos planeado para Descend Into Heaven, así que estén atentos ;)

## Resultados Finales

El juego puede probarse en los siguientes link:

* [Gamejolt - Descend Into Heaven](http://gamejolt.com/games/descend-into-heaven/87079).
* [Itch - Descend Into Heaven](http://spoonmangames.itch.io/descendintoheaven)

Finalmente algunas estadísticas:

* Framework y lenguaje usado: Unity3D 5.1.0 y C#
* Equipo: Dos personas.
* Días de desarrollo: 5 días.
* Horas reales de desarrollo: 2100 minutos, es decir, 35 horas con 15 minutos.
* Líneas de código: 1305.
* Clases creadas: 44.
* Objetivo de aprender Unity: Completado!!

## Conclusión

Unity sin duda es una gran herramienta para el desarrollo de vídeo juegos, su distribución modular y de scripts dan la posibilidad de crear herramientas reutilizables que aceleran el proceso de creación, permitiendo así que los desarrolladores se enfoquen en crear más contenido y de mayor calidad. 

Hay muchas herramientas para trabajar distintas áreas de los vídeo juegos en este engine: el sistema de colisiones físicos está altamente trabajado, la ejecución y manejo de fuentes de sonido es eficiente y fácil de usar, la luz es muy configurable y fácil de dirigir, las animaciones y eventos pueden ser fácilmente controlados mediante máquinas de estados, etc. Sin embargo no existen tutoriales muy detallados sobre estos temas, por lo que si bien es fácil aprender a usarlos, usarlos bien depende de ti.

Aquí en Spoonman Games nos enamoramos de este engine, algunos se arrepienten de no haberlo usado antes, el nivel de profundidad que hemos podido alcanzar usando C# y las herramientas incluidas en el engine nos ha abierto infinitos horizontes. Una vez más nos motivamos con todo a seguir adelante en esta increíble industria!!

Les aseguramos que mientas pase el tiempo y más aprendamos, subiremos tutoriales y herramientas para todos :) Spoonman Games no solo hace juegos para Gamers, también hace herramientas con amor para desarrolladores <3
