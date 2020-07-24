---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---
{% for tag in site.categories %}
  <h3>{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}

<h5>Categories</h5>
{% for category in site.categories %}
    {% assign cat = category[0] %}
    <h6><a href="#">{{ cat }}</a></h6>
    {% for post in site.categories[cat] %}
        <a href="{{ post.url }}">{{ post.title }}</a> <small>{{ post.date }}</small>
    {% endfor %}
{% endfor %}
