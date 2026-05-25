---
layout: single
title: ""
permalink: /writing/
classes: wide
author_profile: true
toc: false
pagination: false
---

<section class="writing-hero">
  <p class="eyebrow">Writing & Technical Articles</p>

  <h1>Explaining quantum ideas through intuition, computation, and research.</h1>

  <p>
    I write about Quantum Computing, Quantum Machine Learning, Information Theory,
    and complex systems with a focus on conceptual clarity and research-oriented thinking.
  </p>
</section>

<div class="writing-stats">
  <div>
    <strong>{{ site.data.articles | size }}</strong>
    <span>Articles</span>
  </div>

  <div>
    <strong>QML</strong>
    <span>Main Focus</span>
  </div>

  <div>
    <strong>Medium / TDS</strong>
    <span>Platforms</span>
  </div>
</div>

## Featured Articles

<div class="article-grid">
{% for article in site.data.articles %}
  <article class="article-card">

    <div class="article-image-wrap">
      <img
        src="{{ article.image }}"
        alt="{{ article.title }}"
        class="article-image"
        loading="lazy"
      >
    </div>

    <div class="article-content">

      <div class="article-meta">
        <span>{{ article.platform }}</span>
        <span>{{ article.date }}</span>
      </div>

      <h3>{{ article.title }}</h3>

      <p>{{ article.description }}</p>

      <div class="text-center">
      <a
        href="{{ article.url }}"
        class="btn btn--primary article-btn"
        target="_blank"
        rel="noopener"
      >
        Read Article →
      </a>
    </div>

      <!-- <a
        href="{{ article.url }}"
        class="btn btn--primary article-btn"
        target="_blank"
        rel="noopener"
      >
        Read Article →
      </a> -->

    </div>
  </article>
{% endfor %}
</div>

## Platforms

<div class="tag-grid">
  <a href="https://medium.com/@dvendator" target="_blank" rel="noopener">Medium</a>
  <a href="https://medium.com/feed/@dvendator" target="_blank" rel="noopener">RSS Feed</a>
  <a href="https://towardsdatascience.com/" target="_blank" rel="noopener">Towards Data Science</a>
</div>