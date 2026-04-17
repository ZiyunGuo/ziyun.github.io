---
layout: default
title: "博客 / Blog"
permalink: /blog/
---

<div class="blog-header animate-fade-in">
  <h1 class="page-title">
    <span class="lang-zh">博客 ✍️</span>
    <span class="lang-en">Blog ✍️</span>
  </h1>
  <span class="post-count">
    {{ site.posts.size }}
    <span class="lang-zh">篇文章</span>
    <span class="lang-en">posts</span>
  </span>
</div>

{% if site.posts.size > 0 %}
  {% for post in site.posts %}
  <article class="post-card animate-fade-in">
    <div class="post-card-meta">
      <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y-%m-%d" }}</time>
      {% for tag in post.tags %}
        <span class="tag">{{ tag }}</span>
      {% endfor %}
    </div>
    <h2 class="post-card-title">
      <a href="{{ post.url }}">{{ post.title }}</a>
    </h2>
    <p class="post-card-excerpt">{{ post.excerpt | strip_html | truncate: 120 }}</p>
    <a href="{{ post.url }}" class="read-more">
      <span class="lang-zh">続きを読む →</span>
      <span class="lang-en">Read more →</span>
    </a>
  </article>
  {% endfor %}
{% else %}
  <div class="card animate-fade-in" style="text-align:center; padding: 3rem;">
    <p style="font-size:2rem;">🌸</p>
    <p style="color:#9b7ab5;">
      <span class="lang-zh">文章正在路上，敬请期待～</span>
      <span class="lang-en">Posts are on the way, stay tuned~</span>
    </p>
  </div>
{% endif %}
