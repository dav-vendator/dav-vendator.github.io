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
  <div class="cv-card">
    <h3>⚛️ {{ article.title }}</h3>
    <p><strong>{{ article.platform }}</strong> · {{ article.date }}</p>
    <p>{{ article.description }}</p>
    <a href="{{ article.url }}" class="btn btn--primary" target="_blank" rel="noopener">Read Article</a>
  </div>
{% endfor %}
</div>


## Platforms

<div class="tag-grid">
  <a href="https://medium.com/@dvendator" target="_blank" rel="noopener">Medium</a>
  <a href="https://medium.com/feed/@dvendator" target="_blank" rel="noopener">RSS Feed</a>
  <a href="https://towardsdatascience.com/" target="_blank" rel="noopener">Towards Data Science</a>
</div>