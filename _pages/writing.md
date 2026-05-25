---
layout: single
title: ""
permalink: /writing/
classes: wide
author_profile: true
toc: false
pagination: false
---

# Writing & Technical Articles

I write about Quantum Computing, Quantum Machine Learning, Information Theory, and complex systems with a focus on intuition and conceptual clarity.


## Featured Articles

<div class="cv-grid">
{% for article in site.data.articles %}
  <article class="article-card">

    <img
      src="{{ article.image }}"
      alt="{{ article.title }}"
      class="article-image"
      loading="lazy"
    >

    <div class="article-content">

      <h3>{{ article.title }}</h3>

      <div class="article-meta">
        {{ article.platform }} · {{ article.date }}
      </div>

      <p>{{ article.description }}</p>
      <p>  
      
      </p>
      <a
        href="{{ article.url }}"
        class="btn btn--primary"
        target="_blank"
        rel="noopener"
      >
        Read Article →
      </a>

      <p>  
      
      </p>

    </div>

  </article>
{% endfor %}
</div>