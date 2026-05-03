---
layout: default
title: "Writing"
permalink: /writing/
---

<div class="page-hero">
  <h1 class="page-hero-title">Writing · 杂谈</h1>
  <p class="page-hero-sub">Essays, notes, and reflections · 随笔与杂谈</p>
</div>

<div class="advice-index-container">
  {% assign sorted_writing = site.writing | sort: 'order' %}
  {% for post in sorted_writing %}
  <a href="{{ post.url | relative_url }}" class="advice-index-card">
    <div class="advice-index-num">{{ post.order | prepend: '0' | slice: -2, 2 }}</div>
    <div class="advice-index-body">
      <h2 class="advice-index-title-en">{{ post.title }}</h2>
      <p class="advice-index-title-zh">{{ post.title_zh }}</p>
      <p class="advice-index-desc">{{ post.description_en }}</p>
    </div>
    <div class="advice-index-arrow">&#8594;</div>
  </a>
  {% endfor %}
</div>
