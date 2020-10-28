---
layout: page
title: archive section
permalink: /archives/
---

{% assign posts = site.posts | where: 'archive', true  %}

<div class="home page">
  <ul class="posts">
    {% for post in posts %}
      <li>
        <span class="post-date">{{ post.date | date: "%b %-d, %Y" }}</span>
        <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
      </li>
    {% endfor %}
  </ul>

</div>
