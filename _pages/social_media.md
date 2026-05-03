---
layout: default
title: "sms"
permalink: /sms/
---

<div class="page-hero">
  <h1 class="page-hero-title">Social Media Posts</h1>
  <p class="page-hero-sub">Writing outside the Academic</p>
</div>

<div class="advice-index-container">
  {% assign sorted_sms = site.sms | sort: 'order' %}
  {% for post in sorted_sms %}
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
