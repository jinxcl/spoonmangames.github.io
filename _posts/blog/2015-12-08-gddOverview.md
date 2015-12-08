---
layout: blogarticle-layout
title: Un vistazo general a los GDD
comments: true
author: victor_gaete
categories:
- blog
tags:
- Blog
image:
    teaser: blog/teaser/gddOverview-teaser.png
    cover: blog/cover/gddOverview-cover.png
---

<p class="margin-top-30">
Hola Spoonmanianos, hoy hablaremos de un tema que nos interesa mucho desarrollar en nuestros futuros proyectos y para hacer honor a nuestras filosofías <b>open mind</b> abriremos un poco las puertas de Descend Into Heaven para que conozcan un poco más como fue el proceso productivo de este juego. Espero que les guste y les sirva :)
</p>

<div class="page-header margin-top-30" markdown='1'>
## Un lugar para juntar todo
</div>

<p class="margin-top-30" markdown='1'>
Generalmente cuando comenzamos el desarrollo de un videojuego nos planteamos varias preguntas que en el transcurso del proceso vamos resolviendo, como por ejemplo:
</p>

 * <p class="margin-top-30">¿Cuántos gráficos necesitaré?</p>
 * <p>¿Qué tipo de música es necesaria?</p>
 * <p>¿Voy a necesitar historia?</p>

<p class="margin-top-30" markdown='1'>
Y  un largo etcétera, entonces naturalmente se genera un montón de información que de alguna manera comienza a apoderarse de nuestros correos, carpetas, papeles, basurero, escritorio, paredes, pizarras etc.
</p>

<p class="margin-top-30" markdown='1'>
Ejemplo:
</p>

<p align="center" class="margin-top-30">
    <img src="{{ site.url }}/img/blog/content/tl-dih-bossfight1.png">
</p>

<p class="margin-top-30" markdown='1'>
Es fácil darse cuenta que debemos utilizar algún método más eficiente para poder almacenar lo que se hace, se piensa o se dice en relación a videojuego.
</p>

<p class="margin-top-30" markdown='1'>
En **Spoonman Games**, en un afán de organizarnos mejor como equipo y empresa, utilizamos Trello para todos nuestros proyectos. Muchos probablemente ya conocen la herramienta, pero para los que no, se puede decir muy resumidamente que Trello es una herramienta colaborativa de gestión de tareas y actividades, es extremadamente flexible y puede adaptarse de la mejor forma que a ti te funcione y a tu equipo.
</p>

<p class="margin-top-30" markdown='1'>
Para darles un ejemplo de cómo organizamos el trabajo. Vean la siguiente imagen.
</p>

<p align="center" class="margin-top-30">
    <img src="{{ site.url }}/img/blog/content/trello-dih.png">
</p>

<p class="margin-top-30" markdown='1'>
Sin embargo, a pesar de que Trello nos sirve para el día a día en la realización del trabajo, es importante concentrar todos lo que se va produciendo de las tareas de una forma más esquematizada y que siga un orden como el que veremos más adelante.
</p>

<p class="margin-top-30" markdown='1'>
Les estoy hablando del **GDD, o en español Documento de diseño de videojuegos**. Cabe mencionar que esta forma de hacer las cosas no es un estándar de la industria y puede mejorarse o modificarse para cada equipo y juego en la que se trabaje, recomendamos la utilización de otras herramientas como la mencionada arriba para poder ir mejorando el documento ya sea para agregar o quitar elementos.
</p>

<div class="page-header margin-top-30" markdown='1'>
## Estructura
</div>

<p class="margin-top-30" markdown='1'>
Para el caso de Descend Into Heaven aplicamos el siguiente esquema para el GDD.
</p>

 * <p class="margin-top-30">Resumen del Proyecto</p>
    * <p>Resumen ejecutivo</p>
    * <p>Concepto</p>
    * <p>Temas centrales</p>
    * <p>Genero</p>
    * <p>Target de audiencia</p>
    * <p>Equipo de desarrollo</p>
    * <p>Información Legal</p>
    * <p>Costos</p>
 * <p>Resumen del Juego</p>
    * <p>Resumen</p>
    * <p>Historia</p>
    * <p>Personajes</p>
    * <p>Resumen de Niveles</p>
 * <p>Gameplay</p>
    * <p>Personajes del Juego</p>
    * <p>Combate</p>
    * <p>Habilidades</p>
    * <p>Items coleccionables</p>
    * <p>Score</p>
    * <p>Horas de juego</p>
    * <p>Condiciones de victoria</p>
 * <p>Layout Menu</p>
    * <p>Definiciones de color</p>
    * <p>Pantalla de Titulo</p>
    * <p>Pantalla de menú</p>
    * <p>Pantalla de Créditos</p>
    * <p>Pantalla de Game Over</p>
 * <p>Game Layout</p>
    * <p>Configuración de cámara</p>
    * <p>Controles de juego</p>
    * <p>Modos de juego</p>
    * <p>Contador de muertes</p>
    * <p>Contador de tiempo</p>
    * <p>Mundos o Niveles</p>
 * <p>Arte y Música</p>
    * <p>Sonido</p>
    * <p>Temas musicales para niveles</p>
    * <p>Efectos de sonido</p>
    * <p>Diseño Personajes</p>
    * <p>Diseño de Bloques</p>
    * <p>Diseño de Piedras</p>
    * <p>Diseño de Ambientes</p>
    * <p>Diseño de acciones</p>

<p class="margin-top-30" markdown='1'>
Como pueden ver, nuestro documento se estructurara con seis grandes pilares:
</p>

 * <p class="margin-top-30" markdown='1'>**Resumen del Proyecto**: en esta sección encontraremos un resumen ejecutivo que permitirá tener claro de una manera global lo que es el juego y sus partes. Es importante tener en cuenta la visión del juego como un proyecto, de forma que es muy importante definir los equipos de trabajo, las programaciones para cada uno de los integrantes e inclusive los costos asociados al proyecto.</p>
 * <p class="margin-top-30" markdown='1'>**Resumen del Juego**: en esta sección se realiza un resumen del juego, explicando la historia, personajes, lista de niveles, mecánicas principales, etc. Es solo un resumen que busca explicar brevemente todo el videojuego, destacando solo lo importante.</p>
 * <p class="margin-top-30" markdown='1'>**Game Play**: en esta sección ya comenzamos a detallar uno por uno los elementos del juego como por ejemplo, lo personajes, habilidades, ítems etc. En esta sección los elementos son detallados mediante diagramas, bocetos, fotos, conceptos y cualquier medio que permita ayudar a materializar cada uno de los puntos expuestos en el punteo.</p>
 * <p class="margin-top-30" markdown='1'>**Layout Menu**: esta sección es una definición mixta entre las definiciones de color y los layouts a utilizar en el juego, esto se definió así para este caso particular debido a que el componente layout estaba directamente relacionado a las definiciones de color a utilizar. Pero para futuros juegos o para sus proyectos esto puede desglosarse en  Graphics y Layouts. Aquí se busca especificar todo lo relacionado con menús en el juego, tales como menú principal, menú de pause, inventarios, tiendas, etc.</p>
 * <p class="margin-top-30" markdown='1'>**Game Layout**: en esta sección básicamente se detallan todos los componentes que forman parte del esqueleto del videojuego, como por ejemplo la definición de las cámaras, controles, interfaces de usuario etc. También se deben especificar los niveles, incluir bocetos e ideas para cada uno de ellos.</p>
 * <p class="margin-top-30" markdown='1'>**Arte y Música**: en esta sección se definirán todos los componentes artísticos, como el diseño de los personajes, ambientes, locaciones etc. Y también los lineamientos auditivos que para cada parte del juego en que sea necesario. Se diferencia respecto del Game Layout en que esta sección solo se preocupa del acabado artístico visual/auditivo.</p>

<div class="page-header margin-top-30" markdown='1'>
## Conclusiones
</div>

<p class="margin-top-30" markdown='1'>
Como pueden ver el crear un GDD es como crear un coloso, sin embargo, es una importante herramienta que nos apoya para organizar y ordenar el desarrollo de nuestros juegos. Queremos destacar el uso de Trello también como herramienta colaborativa para el trabajo diario y un potente aliado para comenzar a armar un buen GDD.
</p>

<p class="margin-top-30" markdown='1'>
Espero que les haya gustado la publicación del día de hoy y que les sea de utilidad este overview del GDD. Nos gustaría entrar en más detalle sobre lo que es un GDD, como armarlo, como utilizarlo y cuando abandonarlo, sin embargo resultaría en una publicación muy larga como para hacerla un blog. Creo que es hora de aprovechar el nuevo diseño de la página de Spoonman Games y crear una sección de artículos! 
</p>

<p class="margin-top-30" markdown='1'>
Nos vemos la próxima semana.
</p>

<p class="margin-top-30" markdown='1'>
Cya Spoon.
</p>

