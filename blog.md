---
title: Blog
permalink: /blog/
description: "Technical posts and learning notes about AI Infra, CUDA, GPU systems, vLLM, Linux, and LLM deployment."
---

<section class="page-hero">
  <p class="eyebrow">Blog</p>
  <h1>Learning notes from the AI Infra path.</h1>
  <p>Short experiments, debugging records, deployment notes, and deeper articles will live here. The point is not to look perfect; the point is to become useful and honest over time.</p>
</section>

<section class="post-list">
  {% for post in site.posts %}
  <article class="post-preview">
    <p>{{ post.date | date: "%Y-%m-%d" }}</p>
    <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    {% if post.description %}<p>{{ post.description }}</p>{% endif %}
    {% if post.tags %}
    <div class="mini-tags">
      {% for tag in post.tags %}<span>{{ tag }}</span>{% endfor %}
    </div>
    {% endif %}
  </article>
  {% else %}
  <p>No posts yet. Start with one real note, even if it is small.</p>
  {% endfor %}
</section>
