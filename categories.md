---
title: Categories
permalink: /categories/
description: "Category index for SZiiN Lab technical notes."
---

<section class="page-title block-section">
  <p class="eyebrow">Categories</p>
  <h1>Browse by topic.</h1>
  <p class="lead">A cleaner way to follow specific threads such as CUDA, vLLM, Linux, systems notes, and meta reflections.</p>
</section>

<section class="block-section">
  {% for category in site.categories %}
  <div class="archive-group" id="{{ category[0] | slugify }}">
    <h2>{{ category[0] }} <span>{{ category[1] | size }}</span></h2>
    <div class="article-list compact-list">
      {% for post in category[1] %}
      <article class="article-row">
        <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y-%m-%d" }}</time>
        <div>
          <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
          {% if post.description %}<p>{{ post.description }}</p>{% endif %}
        </div>
      </article>
      {% endfor %}
    </div>
  </div>
  {% else %}
  <p>No categories yet.</p>
  {% endfor %}
</section>
