---
title: Home
description: "A warm AI Infra engineering blog by SZiiN, focused on CUDA, GPU systems, vLLM, deployment notes, and learning in public."
---

<section class="hero">
  <div class="hero-copy">
    <p class="eyebrow">AI Infra · CUDA · LLM Systems</p>
    <h1>Hi, I'm SZiiN — building a calm corner for GPU experiments, LLM infra notes, and real engineering growth.</h1>
    <p class="hero-lead">
      This is not a cold résumé site. It is a long-term lab notebook for learning in public:
      CUDA kernels, vLLM deployment, Linux debugging, benchmark stories, and the occasional music-fueled reflection.
    </p>
    <div class="hero-actions">
      <a class="button primary" href="{{ '/blog/' | relative_url }}">Read the blog</a>
      <a class="button secondary" href="{{ '/about/' | relative_url }}">Meet the human</a>
    </div>
  </div>
  <aside class="hero-card" aria-label="Current focus">
    <span class="status-dot"></span>
    <p class="card-label">Currently exploring</p>
    <ul>
      <li>LLM inference and serving systems</li>
      <li>GPU performance, CUDA, and profiling</li>
      <li>Reliable Linux environments for experiments</li>
    </ul>
  </aside>
</section>

<section class="section-grid">
  <article class="feature-card">
    <span>01</span>
    <h2>Deep but readable</h2>
    <p>Notes are written for relaxed learning: enough implementation detail to be useful, without turning every post into a paper.</p>
  </article>
  <article class="feature-card">
    <span>02</span>
    <h2>Systems first</h2>
    <p>The blog focuses on practical infrastructure: GPU setup, deployment friction, profiling, throughput, latency, and tradeoffs.</p>
  </article>
  <article class="feature-card">
    <span>03</span>
    <h2>Personal signal</h2>
    <p>Music, late-night debugging, and honest learning logs keep the site human instead of overly corporate.</p>
  </article>
</section>

<section class="content-band">
  <div>
    <p class="eyebrow">Writing map</p>
    <h2>Topics I want to grow into</h2>
  </div>
  <div class="tag-cloud">
    {% for area in site.focus_areas %}
    <span>{{ area }}</span>
    {% endfor %}
    <span>Triton</span>
    <span>Inference Benchmark</span>
    <span>Distributed Systems</span>
  </div>
</section>

<section class="split-section">
  <div>
    <p class="eyebrow">Latest notes</p>
    <h2>Recent posts</h2>
    <div class="post-list compact">
      {% for post in site.posts limit:3 %}
      <a class="post-row" href="{{ post.url | relative_url }}">
        <span>{{ post.date | date: "%Y.%m.%d" }}</span>
        <strong>{{ post.title }}</strong>
      </a>
      {% else %}
      <p>No posts yet. The first CUDA note is warming up.</p>
      {% endfor %}
    </div>
  </div>
  <div class="terminal-card">
    <div class="terminal-bar"><span></span><span></span><span></span></div>
    <pre><code>$ nvidia-smi
$ python benchmark.py --model llama
$ write-note "what actually happened"</code></pre>
  </div>
</section>
