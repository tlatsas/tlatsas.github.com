---
layout: page
title: all posts
permalink: /posts/
---

{% assign posts = site.posts | where_exp: 'post', 'post.archive != true' %}

<div>
  <h1>all posts</h1>
  <ul class="posts">
    {% for post in posts %}
    <li>
      <span class="post-date">{{ post.date | date: "%b %-d, %Y" }}</span>
      <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
    </li>
    {% endfor %}
  </ul>
</div>
