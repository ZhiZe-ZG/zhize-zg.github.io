---
title:  "Pages and Posts of Minimal Mistakes"
date:   2024-03-30 20:05:14
category: Tech-Note/Personal-Website
tags: GitHub-Pages Liquid Jekyll Minimal-Mistakes
header:
  teaser: https://upload.wikimedia.org/wikipedia/commons/2/24/Blank_page_intentionally_end_of_book.jpg
---

The main body of the website generated by Jekyll is a series of static pages. Each page is an HTML file. By default, Jekyll will search for Markdown files in the path where the `_config.yml` file is located and convert them into HTML files and place them on the website. Their access path is generally your website's URL followed by `/` and then the file name (without suffix).

If you think there are some styles or content that are difficult to express using Markdown, you can also write HTML files directly. But whether it is HTML or Markdown, Jekyll will process them before putting them on the website. You can use a language called Liquid to write some markup mixed with your Markdown or HTML. When Jekyll processes these files, it will automatically generate some HTML content for filling based on Liquid markups. For example, a Liquid for-loop can generate a series of similarly formatted HTML paragraphs. For example, the following HTML code containing Liquid will generate a list containing all posts on the website:

```html
{% raw %}
<!--Posts List-->
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
{% endraw %}
```

Since Liquid itself has a lot of content, it is recommended to read the official documentation of Liquid and Jekyll directly to learn how to use Liquid in the Jekyll environment. The official website of Liquid is as follow:

* [Liquid](https://shopify.github.io/liquid/)

The main content of this post is about the page classification of Jekyll and Minimal Mistakes. If you just put all the pages under one path as mentioned above, the path will soon become messy and difficult to manage.

So Jekyll separates a type called "posts" from the pages. A post is a diary or blog, usually with a specific post time. Its content is often about some specific events or subjects. Website pages with specific functions, such as the home page or author introduction page, are still called "pages". Generally speaking, if the website function does not undergo major upgrades, the number of pages will be relatively stable, while posts will accumulate over time. Therefore, the management method for posts is obviously different from pages.

## How Jekyll manages posts

Jekyll will regard the `_post` folder in the website's main directory (the directory where `_config.yml` is located) as the folder where posts are stored.

Each post should be named in the format `<year>-<month>-<day>-<name>.<format>`. In the format, `<year>` is the four-digit year, `<month>` is the two-digit month, and `<day>` is the two-digit day. `<name>` is the name of the article. If the name consists of multiple words, use `-` to separate the words. It should be noted that `<name>` here is mainly used to distinguish files. The title in the actual generated post page is specified by Front Matter within the file. Therefore, I do not recommend making `<name>` too long, as long as they can distinguish several articles written in close time periods. Finally, `format` can be a Markdown suffix `md` or an HTML suffix `html`.

According to Jekyll's default settings, these settings in the posts name determine its access path. Posts written at similar times will be merged into similar paths. But the default setting of Minimal Mistakes is not like this. Regarding the issue of post access paths in Minimal Mistakes, we will discuss later. As a temporary access method, you can put the code listed above on the home page. The default homepage style of Minimal Mistakes also automatically lists all recently written posts.

## Manage Pages with Minimal Mistakes

If you feel that the various pages placed directly in the root directory are too messy, you can use the function provided by Minimal Mistakes to place them into one folder. For configuration methods, please refer to [Working with Pages](https://mmistakes.github.io/minimal-mistakes/docs/pages/).

The main configuration process involves three types of changes: First, create a `_pages` folder and put all functional pages in it. Second, change the Front Matter of each page in `_pages` and specify access paths for them. Third, changing `_config.yml` let Jekyll to include `_pages` in the list of folders that need to be processed (if you have directly copied the default `_config.yml` provided by Minimal Mistakes before, it may already contain a reference to the `_pages` folder.).

Using this method you can create multiple different folders to manage pages for different purposes. For example, if you want to write a book, you can create a `_book` folder and put all relevant chapters in it. Just remember to make corresponding changes in Front Matter and `_config.yml` to ensure that the pages in `_book` can be accessed.

Of course, if you have relatively few pages, you won’t actually use the management methods discussed here.

If you are unfamiliar with concepts such as "Front Matter" mentioned here, you can reread this section after reading the subsequent articles.
