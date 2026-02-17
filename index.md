---
layout: default
title: Home
---

<div class="home">
  <img src="{{ '/assets/images/profile.png' | relative_url }}" class="profile-img" alt="Tay Zar Lin">

  <h1>Hi, it's nice to meet you! 👋</h1>
  <p>Let me explore my passion and share what I learn along the way.</p>

  <div class="about-section">
    <h3>👨‍💻 A little about me</h3>
    <p>Hi, I'm <strong>Tay Zar Lin</strong>. I'm an engineer from Myanmar (Burma), and who has a passion for digital economic velocity. And also, I write code, enjoy memes, and listen music.</p>
    <p>In 2016, I made <a href="#">a website</a> for my friend's company. It was the first step of my journey in the web development field.</p>
  </div>

  <div class="posts-section">
    <h3>✍️ Recent Posts</h3>
    <ul class="post-list">
      {% for post in site.posts limit:5 %}
      <li>
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
        <a class="post-link" href="{{ post.url | relative_url }}">
          {{ post.title | escape }}
        </a>
      </li>
      {% endfor %}
    </ul>

    {% if site.posts.size > 5 %}
      <p><a href="/blog/" class="view-all">View All Posts →</a></p>
    {% endif %}
  </div>
</div>