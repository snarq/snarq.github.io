---
layout: page
title: Vídeos
description: "Gameplays e algo mais!"
permalink: /videos/
meta-robots: "noodp, noydir, noindex, noarchive, follow"
---

{% for post in site.categories.vídeos %}
<div class="post-preview">
    <a href="{{ post.url | prepend: site.baseurl | prepend: site.url }}">
        <h2 class="post-title">
            {{ post.title }}
        </h2>
        {% if post.subtitle %}
        <h3 class="post-subtitle">
            {{ post.subtitle }}
        </h3>
        {% endif %}
    </a>
    <p class="post-meta">Postado por {% if post.author %}{{ post.author }}{% else %}{{ site.title }}{% endif %} em
    {% assign m = post.date | date: "%-m" %}
    {{ post.date | date: "%-d" }} de
    {% case m %}
    {% when '1' %}janeiro
    {% when '2' %}fevereiro
    {% when '3' %}março
    {% when '4' %}abril
    {% when '5' %}maio
    {% when '6' %}junho
    {% when '7' %}julho
    {% when '8' %}agosto
    {% when '9' %}setembro
    {% when '10' %}outubro
    {% when '11' %}novembro
    {% when '12' %}dezembro
    {% endcase %} de
    {{ post.date | date: "%Y" }}
    </p>
</div>
<hr>
{% endfor %}

<!-- Pager -->
{% if paginator.total_pages > 1 %}
<ul class="pager">
    {% if paginator.previous_page %}
    <li class="previous">
        <a href="{{ paginator.previous_page_path | replace: '/index.html', '' | prepend: site.baseurl | prepend: site.url }}/">&larr; Próxima</a>
    </li>
    {% endif %}
    {% if paginator.next_page %}
    <li class="next">
        <a href="{{ paginator.next_page_path | prepend: site.baseurl | prepend: site.url }}/">Anterior &rarr;</a>
    </li>
    {% endif %}
</ul>
{% endif %}
