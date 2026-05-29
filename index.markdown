---
layout: default
title: 🏠 首页
---

<div class="hero-section">
  <h1>欢迎来到 <span class="highlight-name">李娅</span> 的博客</h1>
  <p class="hero-subtitle">Hi~ 我是李娅，一名热爱技术的大三学生 💕</p>
  <a href="/about.html" class="btn">了解更多 →</a>
</div>

<h2>🎓 关于我</h2>
<div class="card about-section">
  <p>我是李娅，就读于云南大学智能科学与技术专业。我热爱编程、人工智能和一切可爱的事物！</p>
  <a href="/about.html" class="btn btn-outline">👀 查看详情</a>
</div>

<h2>📚 最新博客</h2>
{% for post in site.posts limit:3 %}
<div class="card post-card">
  <div class="post-date">📅 {{ post.date | date: "%Y年%m月%d日" }}</div>
  <a href="{{ post.url }}" class="post-title">{{ post.title }}</a>
  <p class="post-excerpt">{{ post.excerpt | strip_html | truncate: 100 }}</p>
</div>
{% endfor %}
<a href="/blog.html" class="btn">查看更多文章 →</a>

<h2>💬 联系我</h2>
<div class="card contact-section">
  <p>邮箱：<a href="mailto:1985717997@qq.com">1985717997@qq.com</a></p>
  <p>GitHub：<a href="https://github.com/liya7827" target="_blank">@liya7827</a></p>
</div>
