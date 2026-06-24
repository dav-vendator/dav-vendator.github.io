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

      {% if project.progress %}
        <div class="project-progress-container">
            <div class="progress-label-row">
            <span>Status: {% if project.progress == 100 %}Stabilized{% else %}Active Development{% endif %}</span>
            <span>{{ project.progress }}%</span>
            </div>
            <div class="progress-bar-bg">
            <div class="progress-bar-fill" style="width: {{ project.progress }}%;"></div>
            </div>
        </div>
      {% endif %}

      {% if project.todo %}
            <div class="project-todo-panel">
                <div class="todo-title">// Project Roadmap </div>
                <ul class="todo-list">
                {% for item in project.todo %}
                    <li class="{% if item.done %}completed{% else %}pending{% endif %}">
                    <span class="todo-checkbox"></span>
                    <span class="todo-task">{{ item.task }}</span>
                    </li>
                {% endfor %}
                </ul>
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