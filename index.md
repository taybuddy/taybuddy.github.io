---
layout: default
title: Home
---

![Tay Zar Lin]({{ '/assets/images/profile.png' | relative_url }}){: .profile-img}

# Hi, it's nice to meet you! 👋

Let me explore my passion and share what I learn along the way.

---

### 👨‍💻 A little about me

Hi, I'm **Tay Zar Lin**. I'm an engineer from Myanmar (Burma), and who has a passion for digital economic velocity. And also, I write code, enjoy memes, and listen music. 

In 2016, I made [a website](#) for my friend's company. It was the first step of my journey in the web development field.

<br>

### ✍️ Recent Posts

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