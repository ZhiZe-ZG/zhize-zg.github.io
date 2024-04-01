---
layout: home
title: ZhiZe' GitHub Pages
---

In nova traditionem intellegere, in vetera innovationem quaerere.

Some tech essays of ZhiZe.

## Posts

* [Index by Categories](./categories)
* [Index by Tags](./tags)
* [Index by Years](./years)

<!-- collections -->

{% assign pure_collections = site.collections | where_exp:"item", "item.label != 'posts'"%}
{% for collection in pure_collections%}
<h2>{{collection.show_name}}<h2>
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
