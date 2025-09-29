---
layout: home
title: "Home"
author_profile: true
paginate: true
---

<section class="magazine">
  <h2>📰 Ultime News</h2>
  {% for post in paginator.posts %}
    {% if post.collection == "news" %}
      <article class="post-preview">
        {% if post.header.image %}
          <a href="{{ post.url }}">
            <img src="{{ post.header.image | relative_url }}" alt="{{ post.title }}">
          </a>
        {% endif %}
        <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
        <p>{{ post.excerpt | strip_html | truncate: 150 }}</p>
        <p><a href="{{ post.url }}">Leggi di più →</a></p>
      </article>
    {% endif %}
  {% endfor %}
</section>

<section class="magazine">
  <h2>🎮 Recensioni</h2>
  {% for recensione in site.recensioni limit:3 %}
    <article class="post-preview">
      {% if recensione.header.image %}
        <a href="{{ recensione.url }}">
          <img src="{{ recensione.header.image | relative_url }}" alt="{{ recensione.title }}">
        </a>
      {% endif %}
      <h3><a href="{{ recensione.url }}">{{ recensione.title }}</a></h3>
      <p>{{ recensione.excerpt | strip_html | truncate: 150 }}</p>
      <p><a href="{{ recensione.url }}">Leggi la recensione →</a></p>
    </article>
  {% endfor %}
</section>

<section class="magazine">
  <h2>📘 Guide</h2>
  {% for guida in site.guide limit:3 %}
    <article class="post-preview">
      {% if guida.header.image %}
        <a href="{{ guida.url }}">
          <img src="{{ guida.header.image | relative_url }}" alt="{{ guida.title }}">
        </a>
      {% endif %}
      <h3><a href="{{ guida.url }}">{{ guida.title }}</a></h3>
      <p>{{ guida.excerpt | strip_html | truncate: 150 }}</p>
      <p><a href="{{ guida.url }}">Leggi la guida →</a></p>
    </article>
  {% endfor %}
</section>
