---
title: Tags
permalink: /tags/
description: "Tag index for SZiiN Lab posts."
---

<section class="page-title block-section">
  <p class="eyebrow">Tags</p>
  <h1>Browse by tag.</h1>
  <p class="lead">Small labels for quickly finding posts across categories.</p>
</section>

<section class="block-section">
  <div class="tag-cloud tag-index">
    {% for tag in site.tags %}
    <a href="#{{ tag[0] | slugify }}">{{ tag[0] }} <span>{{ tag[1] | size }}</span></a>
    {% endfor %}
  </div>

  {% for tag in site.tags %}
  <div class="archive-group" id="{{ tag[0] | slugify }}">
    <h2>{{ tag[0] }}</h2>
    <div class="article-list compact-list">
      {% for post in tag[1] %}
      <article class="article-row">
        <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y-%m-%d" }}</time>
        <div>
          <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        </div>
      </article>
      {% endfor %}
    </div>
  </div>
  {% endfor %}
</section>
