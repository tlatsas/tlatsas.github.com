---
title: blog
layout: master
---

{::options auto_ids="false" /}

blog posts
----------
{:.sub}

{% for post in site.posts %}
* <span class="date light">{{ post.date | date: "%d %b, %Y" }}</span> &raquo; [{{ post.title }}]({{ post.url }})
{:.unstyled .items}
{% endfor %}