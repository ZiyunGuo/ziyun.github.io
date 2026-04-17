---
layout: page
title: "友链 / Friends"
permalink: /friends/
---

<p class="friends-intro animate-fade-in">
  <span class="lang-zh">一些有趣的朋友们 ✨ 欢迎交换友链～</span>
  <span class="lang-en">Some wonderful friends ✨ Feel free to reach out for link exchange~</span>
</p>

<div class="friends-grid">
  {% for friend in site.data.friends %}
  <a class="friend-card animate-fade-in" href="{{ friend.url }}" target="_blank" rel="noopener noreferrer">
    <div class="friend-avatar">
      {% if friend.avatar and friend.avatar != "" %}
        <img src="{{ friend.avatar }}" alt="{{ friend.name }}" loading="lazy" />
      {% else %}
        <span class="friend-avatar-placeholder">{{ friend.name | slice: 0 }}</span>
      {% endif %}
    </div>
    <div class="friend-info">
      <span class="friend-name">{{ friend.name }}</span>
      <span class="friend-desc">{{ friend.school }} · {{ friend.degree }}</span>
      <span class="friend-desc" style="margin-top:0.1rem;">🔬 {{ friend.research }}</span>
    </div>
    <span class="friend-icon" aria-hidden="true">✦</span>
  </a>
  {% endfor %}
</div>

<div style="margin-top:2.5rem;" class="card animate-fade-in">
  <h2 class="section-title">
    <span class="lang-zh">申请友链</span>
    <span class="lang-en">Link Exchange</span>
  </h2>
  <p style="font-size:0.9rem; color: var(--color-muted, #9b7ab5); margin-bottom:0.5rem;">
    <span class="lang-zh">如果想交换友链，欢迎通过以下方式联系我 🌸</span>
    <span class="lang-en">Want to exchange links? Feel free to reach out 🌸</span>
  </p>
  <a href="mailto:zyguo@smu.edu.sg" class="btn btn-outline" style="display:inline-flex;">
    📧 zyguo@smu.edu.sg
  </a>
</div>
