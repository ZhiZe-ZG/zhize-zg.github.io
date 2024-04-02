---
title: "Functional Pages"
date: 2024-04-02 23:24:35 +0800
category: Tech-Note/Personal-Website
tags: GitHub-Pages Jekyll Minimal-Mistakes
---

In previous posts, we roughly divided pages into three categories: posts arranged by date, pages in collections (classified by content), and pages that do not belong to posts or any collection. Pages that not belong to posts or any collection generally have some functionality, so we call them "functional pages" in this posts.

## Homepage

Functional pages are generally placed directly in the root directory of the website project, but in Minimal Mistakes, you can set up folders such as `_pages` to store them. However, there is one functional page that I always place directly in the root directory. That is the homepage of the site (file name `index.md` or `index.html`).

This page is the entrance to the entire website and is displayed by default when someone visits your website (no need add something like `index` after your site address). Exactly how you design your homepage will vary depending on your needs. You can put the index of website content on the homepage, or you can just put some resume information, or you can design your homepage into a beautiful electronic poster.

Minimal Mistakes offers a `home` layout to create a simple homepage. By default it comes with a list of all the posts' links and excerpts. This can make your homepage very long when you have a large number of posts. Fortunately, the home layout of Minimal Mistakes is set up with pagination. This will automatically display the overly long posts list in pagination. However, since the `jekyll-paginate` plugin that provides this functionality only recognizes `index.html`, you must write your home page in HTML format. For more about pagination:

* [Jekyll DOCS: Pagination](https://jekyllrb.com/docs/pagination/)




## 404 Page

