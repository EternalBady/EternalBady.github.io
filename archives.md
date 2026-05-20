---
title: Archives
permalink: /archives/
description: "Chronological archive of SZiiN Lab posts."
---

<section class="page-title block-section">
  <p class="eyebrow">Archives</p>
  <h1>Chronological archive.</h1>
  <p class="lead">A timeline of notes and experiments, inspired by classic engineering logbooks where old posts remain easy to find.</p>
</section>

<section class="block-section">
  {% assign posts_by_year = site.posts | group_by_exp: "post", "post.date | date: '%Y'" %}
  {% for year in posts_by_year %}
  <div class="archive-group">
    <h2>{{ year.name }}</h2>
    <div class="article-list compact-list">
      {% for post in year.items %}
      <article class="article-row">
        <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%m-%d" }}</time>
        <div>
          <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
          {% if post.categories %}<p>{{ post.categories | join: " · " }}</p>{% endif %}
        </div>
      </article>
      {% endfor %}
    </div>
  </div>
  {% endfor %}
</section>
