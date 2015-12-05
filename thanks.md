---
layout: archive
title: ¡Gracias por comunicarte con nosotros!
permalink: /thanks.html
---

Nos tomamos muy enserio todos los mensajes de nuestros fans, haremos sonar las cucharas  <i class="fa fa-spoon"></i><i class="fa fa-spoon"></i><i class="fa fa-spoon"></i><i class="fa fa-music"></i> para que tu mail sea respondido lo más pronto posible ~

<div class="miembros-spoonman">
    <div class="page-footer">
        <ul style="list-style-type: none;">
            {% assign author = site.owner %}                
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
            </div><!-- ./author-content -->
        </ul>
    </div>
</div>

<div class="inline-btn">
    <a class="btn-social twitter" href="https://twitter.com/{{ site.owner.twitter }}" target="_blank"><i class="fa fa-twitter" aria-hidden="true"></i> Spoonman Games en Twitter</a>
    <a class="btn-social facebook" href="https://www.facebook.com/{{ site.owner.facebook }}" target="_blank"><i class="fa fa-facebook" aria-hidden="true"></i> Spoonman Games en Facebook</a>
    <a class="btn-social google-plus"  href="https://plus.google.com/{{ site.owner.googleplus }}" target="_blank"><i class="fa fa-google-plus" aria-hidden="true"></i> Spoonman Games en Google+</a>
</div>

<div class="inline-btn">
    <a class="btn-social twitter" href="https://github.com/{{ site.owner.github }}" target="_blank"><i class="fa fa-github" aria-hidden="true"></i> Spoonman Games en Github</a>
    <a class="btn-social facebook" href="https://www.youtube.com/channel/{{ site.owner.youtube }}" target="_blank"><i class="fa fa-youtube" aria-hidden="true"></i> Spoonman Games en Youtube</a>
</div>