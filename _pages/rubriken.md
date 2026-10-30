---
title: "Rubriken"
permalink: /rubriken/
layout: single
author_profile: true
description: "Die Rubriken im Blog von Tim Schiemann: KI und MCP, SRE-Alltag, Homelab und Laufen, jeweils mit allen Beiträgen."
---

Jeder Beitrag gehört zu genau einer Rubrik. Querverbindungen findest du über die [Schlagwörter](/tags/).

{% assign rubriken = site.data.rubriken %}
{% for rubrik in rubriken %}
<h2 id="{{ rubrik.name | slugify }}">{{ rubrik.name }}</h2>

{{ rubrik.intro }}

{% assign posts = site.categories[rubrik.name] %}
{% if posts and posts.size > 0 %}
<ul>
{% for post in posts %}
  <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a> <small>({{ post.date | date: "%d.%m.%Y" }})</small></li>
{% endfor %}
</ul>
{% else %}
<p><em>Noch keine Beiträge.</em></p>
{% endif %}
{% endfor %}
