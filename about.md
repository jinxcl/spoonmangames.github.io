---
layout: archive
title: Acerca de Spoonman Games
permalink: /about/
image:
    feature: sp-portada.png
members:
- esteban_gaete
- victor_gaete
- corvus
- ragnaroz
- graca
- mitzy
---

Bienvenidos a este rincón de desarrollo de vídeo juegos en el que encontrarás
tips para desarrollar tus propios juegos, códigos fuentes de ayuda, tutoriales,
comentarios y por supuesto **juegos desarrollados por nosotros**!

# Contacto

Si deseas contactarnos directamente para una reunión, conferencia, charla o 
simplemente para hablar de vídeo juegos entra aquí y contáctanos:
<a href="{{ site.url }}/contact/" style="color: red;"><strong>Página de contacto</strong></a>.

<div class="miembros-spoonman">
    <div class="page-footer">
        <ul style="list-style-type: none;">
            {% assign author = site.owner %}                
            <div class="author-image">
                <a href="{{ site.url }}/contact/">
                    {% if author.avatar %}
                       <img src="{{ site.url }}/images/{{ author.avatar }}" alt="{{ author.name }}"/>
                    {% else %}
                        <img src="{{ site.url }}/images/{{ site.owner.avatar }}" alt="{{ site.description }}"/>
                    {% endif %}
                </a>
            </div><!-- ./author-image -->
            <div class="author-content">
                <h3 class="author-name" >
                    {% if author.web %}
                        <a href="{{ site.url }}/contact/" itemprop="author">
                            {{ author.name }}
                        </a>
                    {% else %}
                        <span itemprop="author">{{ author.name }}</span>
                    {% endif %}
                </h3>
                <p class="author-bio">
                    {% if author.rol %}
                        <small>{{ author.rol }}</small><br>
                    {% endif %}
                    {{ author.bio }}
                </p>                    
                <p class="author-social">
                    {% if author.web %}
                        <a href="http://{{ author.web }}" class="badge"><i class="fa fa-home" aria-hidden="true"></i></a>
                    {% endif %}
                    {% if author.email %}
                        <a href="{{ site.url }}/contact/" class="badge inverse"><i class="fa fa-envelope" aria-hidden="true"></i></a>
                    {% endif %}
                    {% if author.facebook %}
                        <a href="https://www.facebook.com/{{ author.facebook }}" class="badge info"><i class="fa fa-facebook" aria-hidden="true"></i></a>
                    {% endif %}
                    {% if author.github %}
                        <a href="https://github.com/{{ author.github }}" class="badge"><i class="fa fa-git" aria-hidden="true"></i></a>
                    {% endif %}
                    {% if author.twitter %}
                        <a href="https://twitter.com/{{ author.twitter }}" class="badge info"><i class="fa fa-twitter" aria-hidden="true"></i></a>
                    {% endif %}
                    {% if author.youtube %}
                        <a href="https://www.youtube.com/channel/{{ author.youtube }}" class="badge danger"><i class="fa fa-youtube-play" aria-hidden="true"></i></a>
                    {% endif %}
                    {% if author.linkedin %}
                        <a href="https://cl.linkedin.com/{{ author.linkedin }}" class="badge info"><i class="fa fa-linkedin" aria-hidden="true"></i></a>
                    {% endif %}
                    {% if author.googleplus %}
                        <a href="https://plus.google.com/u/0/{{ author.googleplus }}" class="badge danger"><i class="fa fa-google-plus" aria-hidden="true"></i></a>
                    {% endif %}
                    {% if author.tumblr %}
                        <a href="https://{{ author.tumblr }}.tumblr.com" class="badge info"><i class="fa fa-tumblr" aria-hidden="true"></i></a>
                    {% endif %}
                    {% if author.instagram %}
                        <a href="https://instagram.com/{{ author.instagram }}" class="badge success"><i class="fa fa-instagram" aria-hidden="true"></i></a>
                    {% endif %}
                    {% if author.blog %}
                        <a href="https://{{ author.blog }}" class="badge"><i class="fa fa-rss" aria-hidden="true"></i></a>
                    {% endif %}
                </p>
            </div><!-- ./author-content -->
        </ul>
    </div>
</div>

{% include toc.html %}

<hr/>
# Historia de Spoonman Games

**Spoonman Games** es un grupo independiente de desarrollo de vídeo juegos que 
nació a finales del año 2010 de la mano de *Esteban Gaete* y *Nikolai Muñoz* 
durante el primer año de universidad cursando la carrera de Ingeniería Civil Informática.

Durante el primer año estas pequeñas cucharitas tuvieron que luchar arduamente
contra la inexperiencia, pero su fuerte determinación y entusiasmo los ayudaron
a seguir adelante! Sin embargo, esta no es una historia de éxito tras éxito... 

En el siguiente año mucha gente se interesó en el proyecto, pero nunca 
lograron mostrar un real interés por el desarrollo de vídeo juegos, lo que 
hacía muy difícil trabajar. Además, la cuchara *Nikolai Muñoz* tuvo 
que dejar los estudios lo que dificultó e hizo aún más lento todo el proceso.

Luego de esto **Spoonman Games** tuvo una pausa de un año, para luego volver a
andar en las manos de *Esteban Gaete* quién decidió usar sus conocimientos
para hacer todo tipo de pruebas en un sin fin de diferentes engines, frameworks
y lenguajes de programación. Durante este periodo de experimentación mucha 
gente apareció para ayudar, pero rápidamente desaparecían.

Durante el año 2014 *Esteban Gaete* y *Nikolai Muñoz* se reunieron para 
intentar darle vida a **Spoonman Games** nuevamente y concentraron sus 
esfuerzos en crear un vídeo juego solo entre ellos dos, pero la ambición los
cegó y armaron un juego demasiado grande como para construirlo en un corto
periodo de tiempo, por lo que el proyecto fue desechado...
<small>*¿o no?*</small>

Y así pasó el tiempo, la cuchara *Esteban Gaete* siguió mejorando sus 
habilidades de programación y de ingeniería en sus estudios hasta que llegó
la gran fecha [**¡15 Mayo del 2015!**]({{ site.url }}/blog/win10gamejam).

**Una nueva era ha comenzado...**

<hr/>
# Miembros de Spoonman Games

Acá encontrarás información y links relevantes de cada uno de los miembros
actuales de este pequeño y modesto grupo de desarrolladores.

<div class="miembros-spoonman">
    <div class="page-footer">
        <ul style="list-style-type: none;">
            {% for member in page.members %}
                {% assign author = site.data.authors[member] %}                
                <div class="author-image">
                    {% if author.avatar %}
                       <img src="{{ site.url }}/images/{{ author.avatar }}" alt="{{ author.name }}"/>
                    {% else %}
                        <img src="{{ site.url }}/images/{{ site.owner.avatar }}" alt="{{ site.description }}"/>
                    {% endif %}
                </div><!-- ./author-image -->
                <div class="author-content">
                    <h3 class="author-name" >
                        {% if author.web %}
                            <a href="http://{{ author.web }}" itemprop="author">
                                {{ author.name }}
                            </a>
                        {% else %}
                            <span itemprop="author">{{ author.name }}</span>
                        {% endif %}
                    </h3>
                    <p class="author-bio">
                        {% if author.rol %}
                            <small>{{ author.rol }}</small><br>
                        {% endif %}
                        {{ author.bio }}
                    </p>                    
                    <p class="author-social">
                        {% if author.web %}
                            <a href="http://{{ author.web }}" class="badge"><i class="fa fa-home" aria-hidden="true"></i></a>
                        {% endif %}
                        {% if author.email %}
                            <a href="mailto:{{ author.email }}" class="badge inverse"><i class="fa fa-envelope" aria-hidden="true"></i></a>
                        {% endif %}
                        {% if author.facebook %}
                            <a href="https://www.facebook.com/{{ author.facebook }}" class="badge info"><i class="fa fa-facebook" aria-hidden="true"></i></a>
                        {% endif %}
                        {% if author.github %}
                            <a href="https://github.com/{{ author.github }}" class="badge"><i class="fa fa-git" aria-hidden="true"></i></a>
                        {% endif %}
                        {% if author.twitter %}
                            <a href="https://twitter.com/{{ author.twitter }}" class="badge info"><i class="fa fa-twitter" aria-hidden="true"></i></a>
                        {% endif %}
                        {% if author.youtube %}
                            <a href="https://www.youtube.com/channel/{{ author.youtube }}" class="badge danger"><i class="fa fa-youtube-play" aria-hidden="true"></i></a>
                        {% endif %}
                        {% if author.linkedin %}
                            <a href="https://cl.linkedin.com/{{ author.linkedin }}" class="badge info"><i class="fa fa-linkedin" aria-hidden="true"></i></a>
                        {% endif %}
                        {% if author.googleplus %}
                            <a href="https://plus.google.com/u/0/{{ author.googleplus }}" class="badge danger"><i class="fa fa-google-plus" aria-hidden="true"></i></a>
                        {% endif %}
                        {% if author.tumblr %}
                            <a href="https://{{ author.tumblr }}.tumblr.com" class="badge info"><i class="fa fa-tumblr" aria-hidden="true"></i></a>
                        {% endif %}
                        {% if author.instagram %}
                            <a href="https://instagram.com/{{ author.instagram }}" class="badge success"><i class="fa fa-instagram" aria-hidden="true"></i></a>
                        {% endif %}
                        {% if author.blog %}
                            <a href="https://{{ author.blog }}" class="badge"><i class="fa fa-rss" aria-hidden="true"></i></a>
                        {% endif %}
                    </p>
                </div><!-- ./author-content -->
            {% endfor %}
        </ul>
    </div>
</div>
