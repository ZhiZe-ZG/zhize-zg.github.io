---
title: "Functional Pages"
date: 2024-04-02 23:24:35 +0800
category: Tech-Note/Personal-Website
tags: GitHub-Pages Jekyll Minimal-Mistakes
header:
  teaser: https://upload.wikimedia.org/wikipedia/commons/0/00/404_Symbol.png
---

In previous posts, we roughly divided pages into three categories: posts arranged by date, pages in collections (classified by content), and pages that do not belong to posts or any collection. Pages that not belong to posts or any collection generally have some functionality, so we call them "functional pages" in this posts.

## Home Page

Functional pages are generally placed directly in the root directory of the website project, but in Minimal Mistakes, you can set up folders such as `_pages` to store them. However, there is one functional page that I always place directly in the root directory. That is the home page of the site (file name `index.md` or `index.html`).

This page is the entrance to the entire website and is displayed by default when someone visits your website (no need add something like `index` after your site address). Exactly how you design your home page will vary depending on your needs. You can put the index of website content on the home page, or you can just put some resume information, or you can design your home page into a beautiful electronic poster.

Minimal Mistakes offers a `home` layout to create a simple home page. By default it comes with a list of all the posts' links and excerpts. This can make your home page very long when you have a large number of posts. Fortunately, the home layout of Minimal Mistakes is set up with pagination. This will automatically display the overly long posts list in pagination. However, since the `jekyll-paginate` plugin that provides this functionality only recognizes `index.html`, you must write your home page in HTML format. For more about pagination:

* [Jekyll DOCS: Pagination](https://jekyllrb.com/docs/pagination/)

## Index Pages

The index pages of posts or collections we introduced earlier are also functional pages.

For posts, we can create 3 different index pages. The first is by categories, and the second is by tags, we have introduced both of them before. The third is indexed by writing years, and its corresponding layout is called `posts`. You just need to create an empty page and set the layout to `posts` (remember to set a permalink for this page).

For collections, create an index page for each collection. If you want to list all collections on one page, try the following Liquid code:

```html
{% raw %}
<!-- collections -->

{% assign pure_collections = site.collections | where_exp:"item", "item.label != 'posts'"%}
{% for collection in pure_collections%}
<h2>{{collection.show_name}}</h2>
  {% for item in collection.docs %}
  <h2>
    <a href="{{ item.url }}">
      {{ item.title }}
    </a>
  </h2>
  {% endfor %}
{% endfor %}
{% endraw %}
```

## Search Page

If you think the category indexing method is not efficient enough, you can also provide a search page. Just create a blank page and set Front Matter like this:

```markdown
---
title: "Search All Posts and Pages"
permalink: /search/
layout: search
author_profile: true
---
```

If you don't want certain pages to be searchable, add `search: false
` to the Front Matter of those pages.

Full text search can be enabled by setting `search_full_content: true` in `_config.yml`. If you set `search: true` in `_config.yml`, a search button will be added to the upper right corner of all pages, which can be used even if there is no search page.

## 404 Page

`404` is an error code that is returned when you visit a page that does not exist on a website. 404 page is the page used as an error message when the page you visit does not exist. You can customize the content displayed on the 404 page by editing `404.html`.

Minimal Mistakes No layout is set for the 404 page. You need to write a 404 page yourself. Here, I add some links to the generated 404 page by `jekyll new` command:

```html
---
permalink: /404.html
layout: default
---

<style type="text/css" media="screen">
  .container {
    margin: 10px auto;
    max-width: 600px;
    text-align: center;
  }

  h1 {
    margin: 30px 0;
    font-size: 4em;
    line-height: 1;
    letter-spacing: -1px;
  }
</style>

<div class="container">
  <h1>404</h1>

  <p><strong>Page not found :(</strong></p>
  <p>The requested page could not be found.</p>
  <p>You can go to <a href="/">homepage</a> or <a href="/search">search</a> what you want.</p>
</div>
```
