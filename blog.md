---
layout: archive
permalink: /blog/
title: Blog
---

Acá podrás encontrar la lista completa de todas las publicaciones de 
**Spoonman Games**, están ordenadas de la más reciente a la más antigua, tan solo has click sobre una de ellas y podrás leer su contenido.

<p class="notice-info" align="justify"><strong>Pro Tip:</strong> Todas las 
publicaciones pueden tener una o más etiquetas (tags), las cuales se encuentran listadas abajo de la fecha de cada publicación. 
Haciendo <strong>click</strong> sobre una de ellas te permitirá acceder a una 
página dónde podrás ver todas las publicaciones bajo la misma etiqueta.</p>

<div class="tiles">
{% for post in site.posts %}
    {% include post-grid.html %}
{% endfor %}
</div><!-- /.tiles -->
