---
layout: article
title: Actualización de Sunset Roboto
comments: true
author: esteban_gaete
categories:
- blog
tags:
- Sunset Roboto
image:
    feature: featured/sr2-featured.png
    teaser: teaser/sr2-teaser.png
summary: 
---

<p class="notice-info" align="justify"><strong>Pro Tip:</strong> Pro tip: Si más de alguno de ustedes ha estado al tanto del <a href="http://impulsagames.com/foro/thread-27.html"><i class="fa fa-book"></i> Devlog de 'Sunset Roboto: The Eternal Rider' en Impulsa Games</a> no leerán nada nuevo aquí ya que este post es para tener un respaldo de las actualizaciones hasta ahora respecto al proyecto. </p>

Actualmente se tiene en funcionamiento las siguientes mecánicas del juego:

 * Background en Loop infinito.
 * Background en cuatro layers con velocidades diferentes.
 * Animación básica de Roboto.
 * Aumento de velocidad al presionar tecla de correr.
 * Barra y contador que muestra la velocidad.
 * Acción y botón de salto.
 * Sol que sube o baja dependiendo si vamos más lento o más rápido.
 * Se pasa de día a tarde y noche dependiendo la posición del sol.
 * Manager para screens como menús o la misma screen de juego.

Esto es principalmente lo hecho durante la Windows 10 Game Jam y se ve de la siguiente manera:

<p align="center"><img src="http://cdn.makeagif.com/media/6-12-2015/bdFPh8.gif"></p>

Los sprites usados son de librerías de assets gratuitos de encontrados en Internet. Desde ese entonces estos son los cambios y avances logrados:

* El proyecto se pasó a Visual Studio 2013 ya que durante la Game Jam se usó Windows 10 y VS2015 R.
* Re-diseño de Roboto, ahora se planea usar un robot sin forma humana, aun no se define bien qué, pero de seguro será algo como una araña o similar.

<p align="center"><img src="http://www.spoonmangames.cl/images/preview/roboto1-preview.png"></p>

* Creación de primeros logos, banner y título.

El logo actual es:
<p align="center"><img src="http://www.spoonmangames.cl/images/sr-teaser.png"></p>

También se ha estado trabajando en varios prototipos relacionados:
<p align="center"><img src="http://www.spoonmangames.cl/images/sr-featured.png"></p>

Creo que es fácil darse cuenta a qué pertenece cada parte de la imagen :3

* Bocetos para el menú principal y la GUI.

<p align="center"><img src="http://www.spoonmangames.cl/images/preview/gui1-preview.JPG"></p>

<p align="center"><img src="http://www.spoonmangames.cl/images/preview/menu1-preview.JPG"></p>

* Bocetos para las animaciones de Roboto.

Por ahora se trabaja en la animación de las piernas principalmente. Ya que Roboto estará corriendo continuamente esto se debe ver bien animado:
<p align="center"><img src="https://trello-attachments.s3.amazonaws.com/557df4698bc31c1c937bd02b/250x200/09476f48e52bfa92b884954b81ce0012/test12frames.gif"></p>

En cuanto al diseño, ha avanzado lento debido a periodos de exámenes pero ya estamos terminando el menú principal, aquí les dejo una pequeña imagen del avance.
<p align="center"><img src="http://www.spoonmangames.cl/images/preview/menu2-preview.png"></p>

Como ya algunos sabrán, hemos liberado una herramienta que estamos usando en Sunset Roboto, está sirve para manejar menús y pantallas de diferente tipo. Acá un link a los interesados: <a href="http://www.spoonmangames.cl/MonoGame-ScreenManager/">ScreenManager para Monogame 3.4</a>.

Lo otro en lo que hemos estado trabajando es en mejorar el movimiento vertical al saltar y en un DebugOutput Manager, este último busca tener una consola en tiempo de ejecución para ver todos los datos de un objeto y como estos varían mientras se ejecuta el juego. En estos momentos estamos haciendo pruebas y se ve así:

<p align="center"><img src="http://www.spoonmangames.cl/images/preview/debug1-preview.gif"></p>

El menú y la GUI han avanzado bastante, pero dejaremos esas actualizaciones para más adelante! 
