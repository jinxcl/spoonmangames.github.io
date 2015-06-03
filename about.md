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

Bienvenidos a este rincón de desarrollo de vídeo juegos en el que encontraras
tips para desarrollar tus propios juegos, códigos fuentes de ayuda, tutoriales,
comentarios y por supuesto **juegos desarrollados por nosotros**!

{% include toc.html %}

<hr/>
# Historia de Spoonman Games

**Spoonman Games** es un grupo independiente de desarrollo de vídeo juegos que 
nació a finales del año 2010 de la mano de *Esteban Gaete* y *Nikolai Muñoz* 
durante el primer año de universidad en el cual se hallaban estudiando 
Ingeniería Civil Informática. 

Durante el primer año estas pequeñas cucharitas tuvieron que luchar arduamente
contra la inexperiencia, pero su fuerte determinación e entusiasmo los ayudaron
a seguir adelante! Sin embargo esta no es una historia de éxito tras éxito... 

Durante el siguiente año de **Spoonman Games** mucha gente se interesó
en el proyecto, pero nunca lograron mostrar un real interés por los vídeo
juegos, lo que hacia muy difícil trabajar en proyectos y además de esto la 
cuchara *Nikolai Muñoz* tuvo que dejar los estudios lo que dificulto e hizo 
más lento todo el proceso.

Luego de esto **Spoonman Games** tuvo una pausa de un año, para luego volver a
andar en las manos de *Esteban Gaete* quién decidió usar sus conocimientos
para hacer todo tipo de pruebas en un sin fin de diferentes engines, frameworks
y lenguajes de programación. Durante este periodo de experimentación mucha 
gente apareció a ayudar, pero luego de un tiempo estas desaparecieron.

Durante el año 2014 *Esteban Gaete* y *Nikolai Muñoz* se reunieron para 
intentar darle vida a **Spoonman Games** nuevamente y concentraron sus 
esfuerzos en crear un vídeo juego solo entre ellos dos, pero la ambición los
cegó y armaron un juego demasiado grande como para construir en un corto
periodo de tiempo por lo que el proyecto fue desechado...
<small>*¿o no?*</small>

Y así paso el tiempo, la cuchara *Esteban Gaete* siguió mejorando sus 
habilidades de programación y de ingeniería en sus estudios hasta que llegó
la gran fecha **¡15 Mayo del 2015!**

**Una nueva era a comenzado...**

<hr/>
# Miembros de Spoonman Games

Acá encontrarás información y links relevantes de cada uno de los miembros
actuales de este pequeño y modesto grupo de desarrolladores :)

<p>
    <br>
    <div class="page-footer">
        <ul style="list-style-type: none;">
            {% for member in page.members %}
                {% assign author = site.data.authors[member] %}                
                <div class="author-image">
                    {% if author.avatar %}
                       <img src="{{ site.url }}/images/{{ author.avatar }}" alt="{{ author.name }}">
                    {% else %}
                        <img src="{{ site.url }}/images/{{ site.owner.avatar }}" alt="{{ site.description }}">
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
                            <a href="https://cl.linkedin.com/in/{{ author.linked }}" class="badge info"><i class="fa fa-linkedin" aria-hidden="true"></i></a>
                        {% endif %}
                        {% if author.googleplus %}
                            <a href="https://plus.google.com/u/0/{{ author.googleplus }}" class="badge danger"><i class="fa fa-google-plus" aria-hidden="true"></i></a>
                        {% endif %}
                        {% if author.tumblr %}
                            <a href="https://{{ author.tumblr }}.tumblr.com" class="badge info"><i class="fa fa-tumblr" aria-hidden="true"></i></a>
                        {% endif %}
                    </p>
                </div><!-- ./author-content -->
            {% endfor %}
        </ul>
    </div>
</p>

<hr/>
# Contactanos

¿Interesado en ser parte de la gran cuchara? o quizás solo deseas saber más
de nosotros o hacer contactos, sea cual sea el caso puedes contactarnos al
siguiente e-mail:

* <p><a href="mailto:spoonman.desarrollo@gmail.com">spoonman.desarrollo@gmail.com</a></p>