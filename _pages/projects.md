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
  <span class="status-badge"><span class="pulse-dot"></span> Core Ecosystems</span>
  <h1>Software Frameworks & Technical Blueprints</h1>
</div>

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

      <!-- Consolidated Progress Tracking Bar -->
      {% if project.progress %}
        <div class="project-progress-container">
          <div class="progress-bar-bg">
            <div class="progress-bar-fill" style="width: {{ project.progress }}%;"></div>
          </div>
        </div>
      {% endif %}

      <!-- Modern Dual Button Action Tray -->
      <div class="project-dual-actions">
        <a href="/projects/{{ project.slug }}/" class="btn btn-details">
          Details &rarr;
        </a>
        <a href="{{ project.repo_url }}" class="btn btn-repo" target="_blank" rel="noopener">
          GitHub
        </a>
      </div>

    </div>
  {% endfor %}
</div>