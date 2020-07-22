---
layout: page
title: About Me
permalink: /about/
---

To know more about me, visit my [website](https://mzaidi59.github.io/).
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
