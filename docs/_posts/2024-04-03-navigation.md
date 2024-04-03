---
title: "Navigation Settings in Minimal Mistakes"
date: 2024-04-03 19:05:51 +0800
category: Tech-Note/Personal-Website
tags: GitHub-Pages Jekyll Miminal-Mistakes Front-Matter
header:
  teaser: https://upload.wikimedia.org/wikipedia/commons/b/b4/Compass_on_the_Brig_Roald_Amundsen.jpg
---

Long articles without navigation are difficult to read. Websites with many pages without navigation are also difficult to use. In this post we will introduce the navigation function provided by Minimal Mistakes.

## TOC (Table Of Contents)

For a single article, you can use TOC as article navigation. The setting method is very simple, you only need to add `toc: true` to the Front Matter of the article. This will generate a TOC on the right of your page. Additionally, you can use `toc_sticky: true` to make the TOC move with your screen. This prevents you from losing TOC after scrolling down a few paragraphs. These two options are very useful and I usually set them as the default options for article pages.

Note that the TOC is automatically generated based on the heading marks in the article. If you do not use heading marks (such as `##` in Markdown and `<h2>` in HTML), the TOC will not include valid content.

For more see:

* [Minimal Mistakes: Single laytout - Table of contents](https://mmistakes.github.io/minimal-mistakes/docs/layouts/#table-of-contents)

## Sidebar Navigation

From here we introduce the navigation for the website structure. The first is the navigation displayed in the left sidebar. This is not generate automatically. We need to describe the navigation content to be displayed in a data file. This file should be located in `_data` and named as `navigation.yml`. For example:

```yaml
overall:
  - title: Post Indexes
    children:
      - title: "Post Index by Years"
        url: /years/
      - title: "Post Index by Categories"
        url: /categories/
      - title: "Post Index by Tags"
        url: /tags/
      
  - title: Knowledge Taxonomy
    children:
      - title: "Knowledge Taxonomy Index"
        url: /knowledge-taxonomy/
      - title: "Languages Index"
        url: /languages/
      - title: "Histories Index"
        url: /histories/
      - title: "Thoughts Index"
        url: /thoughts/
      - title: "Sciences Index"
        url: /sciences/

  - title: Tools
    children:
      - title: "Search"
        url: /search/
```

The `overall` is the name of the sidebar navigation definition. You can define different navigations in this file for different pages.

After completing the definition, add a reference to the navigation in the Front Matter of the page where the sidebar navigation needs to be displayed. For example:

```yaml
sidebar:
  nav: overall
```

In addition to displaying navigation, the sidebar can also display the author information. Author information is defined in `_config.yml`. To enable sidebar author information for the page, add `author_profile: true` (this item do not belong to the `sidebar` item).

For more about sidebars, see:

* [Minimal Mistakes: Layouts - Sidebars](https://mmistakes.github.io/minimal-mistakes/docs/layouts/#sidebars)

## Masthead Navigation

Minimal Mistakes also provides masthead navigation, which is the navigation displayed at the top of the pages. Compared with the sidebar navigation, this kind of navigation is more eye-catching but can accommodate fewer items.

Define a navigation named `main` in `navigation.tml`, the content of which will be automatically displayed on the masthead of all pages. For example:

```yaml
main:
  - title: "Posts"
    url: /year/
  - title: "Categories"
    url: /categories/
  - title: "Tags"
    url: /tags/
```

For more see:

* [Minimal Mistakes: Navigation](https://mmistakes.github.io/minimal-mistakes/docs/navigation/)
