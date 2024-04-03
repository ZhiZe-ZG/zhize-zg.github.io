---
title: "Introduction of Jekyll Front Matter"
date: 2024-03-30 23:38:53 +0800
category: Tech-Note/Personal-Website
tags: GitHub-Pages Jekyll Front-Matter
header:
  teaser: https://jekyllrb.com/img/logo-2x.png
---

Both Markdown and HTML are markup languages that tend to represent information on the page that is displayed to humans. The content is either directly displayed on the final page, or a description of the style of the displayed content. However, during the automatic generation of pages, there is some information that helps the program automatically process it, but does not necessarily need to be displayed on the page. For example, the writing time and classification of an article do not necessarily need to be displayed on the final page, but for websites that need to be indexed, this information is necessary for each page. This kind of information that is automatically processed by the program and does not necessarily appear on the final page is called "metadata".

In order to enhance the ability of HTML and Markdown to store metadata, Jekyll adds a module called Front Matter for them.

You can learn about Front Matter on the official Jekyll page:

* [Jekyll DOCS: Front Matter](https://jekyllrb.com/docs/front-matter/)

In this post I will briefly introduce some of the key points in my opinion.

## Grammar of Front Matter

Front Matter is a block marked by `---` at the beginning of the file. In the Front Matter block, we can use YAML syntax to record metadata.

You can customize variable names in Front Matter and then reference them through Liquid in the page. But this is a little complicated for us now. We first have to figure out the usage of the variables defined by Jekyll or the theme. For example, setting `published` to false will allow Jekyll to hide the page in the generated website:

```yaml
---
title: "Introduction of Jekyll Front Matter"
date: 2024-03-30 23:38:53 +0800
category: Tech-Note/Personal-Website
tags: GitHub-Pages Jekyll Front-Matter
published: false
---
```

This is a Jekyll predefined global variable that can be used to hide unfinished pages.

## title

The variable `title` is not a predefined variable, but many themes or page templates use it. It represents the title of an article, which will appear on the article page or various automatically generated index pages.

If this item on the post page is empty, the `<name>` part of the post file name will be used to replace the title.

Content marked with `#` in Markdown or `h1` in HTML will only be treated as ordinary paragraphs and will not appear as article titles on various automatically generated index pages. However, the display effect of title in most themes is the same as `h1`, so it is recommended that if you want to use `h` tags (or `#` marks in Markdown) in articles, start with `h2` (or `##`).

## date

The variable `date` is one of the variables predefined by Jekyll for posts. It is used to accurately specify the writing time of an article, making it easy to index posts by time. When `date` is set, the writing time specified in the original file name will be ignored by the indexes.

The format of the date value is `YYYY-MM-DD HH:MM:SS ±TTTT`. The letters in front represent the year, month, day, hour, minute and second respectively. It should be explained that `±TTTT` should be replaced by the time zone code. The time zone code consists of a positive or negative sign followed by four digits. A `+` indicates that the time zone is before UTC, and a `-` indicates that it is after UTC. The four-digit number represents the number of hours and minutes from UTC. For example, `+0900` means UTC+09:00.

## permalink

Jekyll has a set of rules that automatically generate corresponding web page access paths based on file paths and file names. If you want to directly specify an access path to the page, you can use the `permalink` variable.

For example, if I set the following settings for a page in my website, then its access path is <https://www.zhize.xyz/categories/>:

```yaml
permalink: /categories/
```

(my website address is `https://www.zhize.xyz`.)

## layout

Jekyll will use some configured page templates when generating page files. The article content you write in the file will be filled into the page template. To specify which template your page is generated from, use the `layout` variable.

If you specify a `layout` but the displayed effect does not have any template style, please check whether the theme you are using provides a template with that name.

Generally speaking, the page template of the theme will be placed in the `_layout` folder. You can also create this folder in your own root directory and put your own templates in it. If your self-made template has the same name as the template provided by the theme, your self-made template will overwrite the theme template. This logic also applies to other configurations provided by themes or Jekyll.

## Setting Default Front Matter Values

Writing a lengthy Front Matter for each page is quite a bit of work. So Jekyll allows you to set default values for the page's Front Matter in `_config.yml`.

You can refer to [Front Matter Defaults](https://jekyllrb.com/docs/configuration/front-matter-defaults/) to write this type of configuration.

The `defaults` of `_config.yml` consists of multiple items. Each project consists of two parts. The `scope` part indicates the path and page type that the rules can apply. The `values` part represents the variables to be filled and their default values.

It should be noted that the `type` here is not a simple variable name, but the name of the collection. We will discuss Jekyll’s collections later.
