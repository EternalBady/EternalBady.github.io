---
title: Blog
permalink: /blog/
description: "Technical posts and learning notes about AI Infra, CUDA, GPU systems, vLLM, Linux, and LLM deployment."
---

<section class="page-title block-section">
  <p class="eyebrow">Blog</p>
  <h1>Learning notes from the AI Infra path.</h1>
  <p class="lead">Short experiments, debugging records, deployment notes, and deeper articles live here. The point is not to look perfect; the point is to become useful and honest over time.</p>
</section>

<section class="block-section">
  <div class="section-heading inline-heading">
    <div>
      <p class="eyebrow">All posts</p>
      <h2>Reverse chronological log</h2>
    </div>
    <a class="text-link" href="{{ '/feed.xml' | relative_url }}">RSS →</a>
  </div>
  <div class="article-list">
    {% for post in site.posts %}
    <article class="article-row">
      <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y-%m-%d" }}</time>
      <div>
        <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        {% if post.description %}<p>{{ post.description }}</p>{% endif %}
        {% if post.tags %}
        <div class="mini-tags">
          {% for tag in post.tags %}<a href="{{ '/tags/' | relative_url }}#{{ tag | slugify }}">{{ tag }}</a>{% endfor %}
        </div>
        {% endif %}
      </div>
    </article>
    {% else %}
    <p>No posts yet. Start with one real note, even if it is small.</p>
    {% endfor %}
  </div>
</section>
