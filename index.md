---
layout: default
---

# Inside

<ul>
  {% for post in site.posts %}
    <li>
      <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
      <p>{{ post.description }}</p>
      <a href="{{ post.url | relative_url }}">Read more...</a>
    </li>
  {% endfor %}
</ul>

