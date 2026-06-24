---
layout: single
title: "VLib"
permalink: /projects/vlib/
classes: wide
author_profile: true
toc: false
---

<div class="project-back-nav">
  <a href="/projects/">&larr; Back to Projects</a>
</div>

<div class="project-deep-hero">
  <span class="status-badge"><span class="pulse-dot"></span> Core Systems Project</span>
  <h1>VLib &mdash; Modern C++ Numerical Computing Library</h1>
  <p class="hero-abstract">
    A from-scratch C++20 numerical computing library built to explore memory
    management, custom containers, linear algebra, tensor computation, and the
    systems foundations behind high-performance machine learning libraries.
  </p>
</div>

<div class="project-dashboard-grid">

  <div class="project-main-specs">

    <h2>Architectural Overview</h2>
    <p>
      VLib is a hands-on systems project focused on understanding how numerical
      and machine learning libraries are built beneath the surface. Instead of
      treating vectors, matrices, tensors, memory ownership, and strides as black
      boxes, the library implements these components from first principles in
      modern C++.
    </p>

    <p>
      The goal is not to replace mature libraries like NumPy, Eigen, or PyTorch.
      The goal is to build the core abstractions myself: owning containers,
      linear algebra primitives, tensor storage, shape metadata, stride-based
      indexing, and eventually view-based slicing and broadcasting.
    </p>

    <div class="tech-spec-callout">
      <h3>// Toolchain</h3>
      <ul>
        <li><strong>Language:</strong> Modern C++20</li>
        <li><strong>Compiler:</strong> Clang / GCC with C++20 support</li>
        <li><strong>Focus:</strong> Memory ownership, containers, linear algebra, tensors, and performance-aware design</li>
      </ul>
    </div>

    <h2>Core Engineering Subsystems</h2>

    <h3>1. Custom Memory Ownership</h3>
    <p>
      VLib starts with smart pointer implementations to understand ownership,
      move semantics, reference counting, resource lifetime, and RAII. These
      components form the conceptual base for managing dynamically allocated
      numerical data safely.
    </p>

    <h3>2. STL-style Containers</h3>
    <p>
      The library includes a custom dynamic vector implementation with capacity
      management, copy and move semantics, initializer-list construction,
      indexing, and iterator-style access. This provides the base abstraction
      for contiguous numerical storage.
    </p>

    <h3>3. Matrix Operations</h3>
    <p>
      The matrix module builds on contiguous memory layouts to support basic
      linear algebra operations, element access, construction, copying, moving,
      and formatted output. It serves as the bridge between simple containers
      and higher-dimensional tensor abstractions.
    </p>

    <h3>4. Tensor Computation</h3>
    <p>
      The tensor module extends the design to N-dimensional data using shape
      metadata, stride computation, offset mapping, and contiguous storage. This
      is the current active development focus and will later support TensorView,
      slicing, transpose, and broadcasting semantics.
    </p>

    <h2>Why I Built This</h2>
    <p>
      Building VLib is my way of understanding the machinery behind libraries
      like NumPy and PyTorch. Concepts such as tensor strides, views, transposes,
      and broadcasting become much clearer when implemented directly instead of
      only used through high-level APIs.
    </p>

  </div>

  <div class="project-sidebar-monitor">

    <div class="sidebar-console-card">
      <h3>// Project Registry</h3>
      <table class="console-meta-table">
        <tr><td><strong>Status:</strong></td><td>Active Development</td></tr>
        <tr><td><strong>Version:</strong></td><td>v0.4-alpha</td></tr>
        <tr><td><strong>License:</strong></td><td>MIT Open Source</td></tr>
        <tr><td><strong>Language:</strong></td><td>C++20</td></tr>
      </table>

      <a href="https://github.com/dav-vendator/vlib" class="btn cv-btn-primary full-width-btn" target="_blank" rel="noopener">
        Open GitHub Repository
      </a>
    </div>

    <div class="sidebar-console-card">
      <div class="project-progress-container">
        <div class="progress-label-row">
          <span>Implementation Progress</span>
          <span>45%</span>
        </div>
        <div class="progress-bar-bg">
          <div class="progress-bar-fill" style="width: 45%;"></div>
        </div>
      </div>
    </div>

    <div class="project-todo-panel">
      <div class="todo-title">// Development Roadmap</div>
      <ul class="todo-list">
        <li class="completed">
          <span class="todo-checkbox"></span>
          <span class="todo-task">Smart pointer implementations</span>
        </li>
        <li class="completed">
          <span class="todo-checkbox"></span>
          <span class="todo-task">Vector container implementation</span>
        </li>
        <li class="completed">
          <span class="todo-checkbox"></span>
          <span class="todo-task">Matrix class and operations</span>
        </li>
        <li class="pending">
          <span class="todo-checkbox"></span>
          <span class="todo-task">Tensor container implementation</span>
        </li>
        <li class="pending">
          <span class="todo-checkbox"></span>
          <span class="todo-task">TensorView and slicing</span>
        </li>
        <li class="pending">
          <span class="todo-checkbox"></span>
          <span class="todo-task">Broadcasting support</span>
        </li>
        <li class="pending">
          <span class="todo-checkbox"></span>
          <span class="todo-task">Benchmark suite validation</span>
        </li>
      </ul>
    </div>

  </div>
</div>