---
layout: archive
permalink: /
title: "Latest Posts"
image:
 feature: teaser.png
---

<div class="tiles">
{% for post in site.posts %}
	{% include post-grid.html %}
{% endfor %}
</div><!-- /.tiles -->