---
layout: home
title: ZhiZe' GitHub Pages
---

Some tech essays of ZhiZe.

## Posts

* [Category Archive](./categories)
* [Tag Archive](./tags)
* [Year Archive](./years)

<!-- collections -->

{% assign pure_collections = site.collections | where_exp:"item", "item.label != 'posts'"%}
{% for collection in pure_collections%}
<h2>{{collection.label}}<h2>
{% for item in collection.docs %}
  <h2>
    <a href="{{ item.url }}">
      {{ item.title }}
    </a>
  </h2>
{% endfor %}
{% endfor %}


 <!-- {{ item.title }} - {{ item.position }} -->

  <!-- <p>{{ item.content | markdownify }}</p> -->

<!--Posts List-->
<!-- <ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul> -->
