---
layout: page
title: Vídeos
description: "Gameplays e algo mais!"
permalink: /videos/
meta-robots: "noodp, noydir, noindex, noarchive, follow"
---
{% for post in site.categories.videos %}
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