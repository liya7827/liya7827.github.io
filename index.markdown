---
layout: cute
title: My Cute Blog
---

<div class="hero-section">
  <h1>🌸 My Cute Blog 🌸</h1>
  <p class="hero-subtitle">Welcome to my lovely little corner of the internet! 💖</p>
  <a href="#posts" class="btn">Let's Explore! 🚀</a>
</div>

## 🌟 About Me 🌟

<div class="card about-section">
  <h2>Hi there! I'm a cute blogger! 🥰</h2>
  <p>I love sharing my thoughts, ideas, and all the cute things in life! Here you'll find posts about tech, lifestyle, and everything that makes me smile.</p>
  
  <h3>My Favorite Things 🎀</h3>
  <ul class="skills-list">
    <li>🎨 Design</li>
    <li>💻 Coding</li>
    <li>📚 Reading</li>
    <li>🌸 Flowers</li>
    <li>🐱 Cats</li>
    <li>🍰 Desserts</li>
  </ul>
</div>

## ✨ Latest Posts ✨

<section id="posts">
  {% for post in site.posts %}
  <article class="card post-card">
    <time class="post-date">📅 {{ post.date | date: "%Y年%m月%d日" }}</time>
    <h2><a href="{{ post.url | relative_url }}" class="post-title">{{ post.title }}</a></h2>
    <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
    <a href="{{ post.url | relative_url }}" class="btn btn-outline">Read More →</a>
  </article>
  {% endfor %}
</section>

## 📬 Contact Me 📬

<div class="card contact-section">
  <h2>Let's be friends! 💝</h2>
  <p>Feel free to reach out to me anytime!</p>
  <div class="contact-links">
    <a href="mailto:your-email@example.com">📧 Email</a>
    <a href="https://github.com/yourusername" target="_blank">💼 GitHub</a>
    <a href="https://twitter.com/yourusername" target="_blank">🐦 Twitter</a>
  </div>
</div>