---
layout: home
title: ZhiZe' GitHub Pages
---

Some tech essays of ZhiZe.

Posts:

* [Category Archive](./categories)
* [Tag Archive](./tags)
* [Year Archive](./years)

Collections:

{% for staff_member in site.knowledge-taxonomy %}
  <h2>
    <a href="{{ staff_member.url }}">
      {{ staff_member.title }} - {{ staff_member.position }}
    </a>
  </h2>
  <p>{{ staff_member.content | markdownify }}</p>
{% endfor %}

<!--Posts List-->
<!-- <ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul> -->
