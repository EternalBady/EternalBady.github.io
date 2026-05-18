---
title: Home
description: "A structured AI Infra engineering logbook by SZiiN, focused on CUDA, GPU systems, vLLM, deployment notes, projects, and learning in public."
---

<section class="home-hero block-section">
  <div class="hero-text">
    <p class="eyebrow">Personal Engineering Logbook</p>
    <h1>SZiiN's AI Infra notes, CUDA experiments, and LLM systems journal.</h1>
    <p class="lead">A professional but relaxed home for technical growth: reproducible notes, deployment lessons, benchmark stories, and projects that show the actual engineering path.</p>
    <div class="hero-actions">
      <a class="button primary" href="{{ '/blog/' | relative_url }}">Start Reading</a>
      <a class="button secondary" href="{{ '/projects/' | relative_url }}">View Projects</a>
    </div>
  </div>
  <div class="hero-summary">
    <h2>Current Focus</h2>
    <ul class="check-list">
      <li>LLM inference and serving systems</li>
      <li>CUDA, GPU profiling, and performance intuition</li>
      <li>Linux environments that are repeatable and explainable</li>
      <li>Learning in public without making readers feel pressured</li>
    </ul>
  </div>
</section>

<section class="block-section">
  <div class="section-heading">
    <p class="eyebrow">Who am I</p>
    <h2>An AI Infra learner with a systems mindset and a human voice.</h2>
  </div>
  <div class="text-columns">
    <p>I am SZiiN, also known as EternalBady. My direction is AI Infra / LLM Infra: GPU systems, inference deployment, CUDA notes, benchmark analysis, and the small debugging details that make engineering real.</p>
    <p>This site is meant to feel like a serious logbook rather than a cold résumé. It should be readable, structured, a little hacker-like, and still warm enough that people can learn comfortably.</p>
  </div>
</section>

<section class="block-section">
  <div class="section-heading inline-heading">
    <div>
      <p class="eyebrow">Writing Map</p>
      <h2>Clear sections for long-term growth</h2>
    </div>
    <a class="text-link" href="{{ '/categories/' | relative_url }}">Browse categories →</a>
  </div>
  <div class="category-grid">
    {% for item in site.featured_categories %}
    <article class="category-card">
      <h3>{{ item.name }}</h3>
      <p>{{ item.description }}</p>
    </article>
    {% endfor %}
  </div>
</section>

<section class="block-section recent-section">
  <div class="section-heading inline-heading">
    <div>
      <p class="eyebrow">Recently</p>
      <h2>Latest notes</h2>
    </div>
    <a class="text-link" href="{{ '/archives/' | relative_url }}">Archives →</a>
  </div>
  <div class="article-list">
    {% for post in site.posts limit:5 %}
    <article class="article-row">
      <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y-%m-%d" }}</time>
      <div>
        <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        {% if post.description %}<p>{{ post.description }}</p>{% endif %}
      </div>
    </article>
    {% else %}
    <p>No posts yet. The first CUDA note is warming up.</p>
    {% endfor %}
  </div>
</section>

<section class="block-section lab-section">
  <div>
    <p class="eyebrow">Lab Notebook</p>
    <h2>What a good post should contain</h2>
    <p class="lead small-lead">A note is useful when it records context, commands, observations, tradeoffs, and what I would do differently next time.</p>
  </div>
  <pre class="terminal-card"><code>$ nvidia-smi
$ python benchmark.py --model llama --serve vllm
$ write-note --include commands,metrics,mistakes</code></pre>
</section>
