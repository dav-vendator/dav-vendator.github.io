---
layout: single
title: ""
permalink: /projects/
classes: wide
author_profile: true
toc: false
pagination: false
---

<div class="project-hero">
  <span class="status-badge"><span class="pulse-dot"></span> Research & Development</span>
  <h1>Research, Engineering & Open Source Projects</h1>
  <p>
    From quantum machine learning architectures to modern C++ libraries,
    these projects represent my work at the intersection of research and software engineering.
  </p>
</div>

## Featured Ecosystems

<div class="project-matrix">
  {% for project in site.data.projects %}
    <div class="project-card {% if project.featured %}featured{% endif %}">
      
      <div class="project-header-row">
        <span class="tech-pill {{ project.tech_class }}">{{ project.tech_label }}</span>
        <span class="repo-meta">// {{ project.repo_index }}</span>
      </div>

      <h3>{{ project.title }}</h3>
      
      <p class="project-description">{{ project.description }}</p>
      
      {% if project.tags %}
      <div class="project-tags">
          {% for tag in project.tags %}
          <span class="tag-{{ tag | slugify }}">{{ tag }}</span>
          {% endfor %}
      </div>
      {% endif %}

      <div class="project-action-tray">
        <a href="{{ project.url }}" class="btn project-link-btn" target="_blank" rel="noopener">
          {% if project.featured %}Source Repository &rarr;{% else %}Explore Design{% endif %}
        </a>
      </div>

    </div>
  {% endfor %}
</div>