---
layout: default
title: home
---
<div class="home">
    <img src="{{ '/assets/images/profile.png' | relative_url }}" class="profile-img" alt="Tay Zar Lin">

    <h1> Hi, it's nice to meet you! 👋 </h1>
    <p>Let me explore my passion and share what I learn along the way.</p>

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
            <h3>
            <a class="post-link" href="{{ post.url | relative_url }}">
                {{ post.title | escape }}
            </a>
            </h3>
        </li>
        {% endfor %}
    </ul>

    {% if site.posts.size > 5 %}
        <p><a href="/blog/">View All Posts →</a></p>
    {% endif %}

</div>