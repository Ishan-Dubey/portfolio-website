---
layout: page
title: Blog
permalink: /blog/
---

<h1 class="page-title">Blog</h1>
<p class="page-description">
  Welcome to my blog—where I share deep dives, tutorials, and project updates on Rust, AI, and real-world coding challenges.
</p>

<!-- Top: posts-per-page selector -->
<div class="posts-per-page-top">
  <label for="posts-per-page" class="ppp-label">
    Posts per page:
    <select id="posts-per-page">
      <option value="3" selected>3</option>
      <option value="5">5</option>
      <option value="10">10</option>
    </select>
  </label>
</div>

<div class="pagination-bar">
  <button class="page-nav first-page">First</button>
  <button class="page-nav prev-page">Prev</button>
  <div class="pagination-buttons"></div>
  <button class="page-nav next-page">Next</button>
  <button class="page-nav last-page">Last</button>
</div>

<ul class="posts-list">
  {% for post in site.posts %}
    <li class="post-list-item">
      <a href="{{ post.url | relative_url }}" class="post-link">
        {% if post.thumbnail %}
          <img
            src="{{ post.thumbnail | relative_url }}"
            alt="{{ post.title }} thumbnail"
            class="post-thumbnail"
          >
        {% endif %}
        <div class="post-content">
          <h2>{{ post.title }}</h2>
          <p>{{ post.excerpt | strip_html | truncate:150 }}</p>
          <small>{{ post.date | date: "%b %-d, %Y" }}</small>
        </div>
      </a>
    </li>
  {% endfor %}
</ul>

<!-- Bottom: pagination bar -->
<div class="pagination-bar">
  <button class="page-nav first-page">First</button>
  <button class="page-nav prev-page">Prev</button>
  <div class="pagination-buttons"></div>
  <button class="page-nav next-page">Next</button>
  <button class="page-nav last-page">Last</button>
</div>

