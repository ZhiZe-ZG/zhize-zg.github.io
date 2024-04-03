---
title: "Post Categories and Tags"
date: 2024-03-31 01:34:29 +0800
category: Tech-Note/Personal-Website
tags: GitHub-Pages Jekyll Front-Matter Minimal-Mistakes
header:
  teaser: https://upload.wikimedia.org/wikipedia/commons/thumb/c/c5/13-11-02-olb-by-RalfR-03.jpg/640px-13-11-02-olb-by-RalfR-03.jpg
---

In this post, we will discuss taxonomy of posts. Jekyll provides two default Front Matter variables for taxonomy of posts. Categoties are used to build tree-like taxonomy, while Tags are used to build multiple-label taxonomy.

The following official documents are for reference:

* [Front Matter - Predefined Variables for Posts](https://jekyllrb.com/docs/front-matter/#predefined-global-variables)
* [Minimal Mistakes Configuration - Archive Settings](https://mmistakes.github.io/minimal-mistakes/docs/configuration/#archive-settings)

## Categories

Jekyll provides two variable names for category taxonomy: `categories` and `category`. Only use the singular form for personal recommendations. In the plural version, multiple category names are not in a parallel relationship but in a hierarchical relationship. But when using the categories archive function of Minimal Mistakes, this hierarchical relationship will not be reflected.

Spaces in `category` are considered separators for different `category` values. If you want to use a single `category` to represent a hierarchical relationship, you can use `/` to separate its value. For example:

```yaml
category: Tech-Note/Personal-Website
```

It should be noted that `category` will change the access path of the page. By default, Jekyll sets the access path of posts to include the writing time and title of the file (Minimal Mistakes omits the writing time by default, you can change it by modifying `permalink` in `_config.yml` refer to [Jekyll DOCS: Permalinks](https://jekyllrb.com/docs/permalinks/)). When `category` is specified, the post access path consists of `category` and the title in the file name. In addition, if both `category` and `permalink` exist in Front Matter, the access path of the post is determined by `permalink`.

For example, the access path to this post is:

```url
https://www.zhize.xyz/Tech-Note/Personal-Website/post-categories-and-tags/
```

`https://www.zhize.xyz` is my website address.

The file name of this post is `2024-03-31-post-categories-and-tags.md`.

The Front Matter of this post is as follows:

```markdown
---
title: "Post Categories and Tags"
date: 2024-03-31 01:34:29 +0800
category: Tech-Note/Personal-Website
tags: GitHub-Pages Jekyll Front-Matter Minimal-Mistakes
---
```

## Tags

If we use an analogy in object-oriented terms, the taxonomy provided by categories are similar to single inheritance of classes, while the taxonomy provided by tags are similar to multiple inheritance of interfaces.

The variable name of Tags is `tags`. Spaces are used to separate multiple different tags. Since tags do not change the access address of the post, a post can have multiple tags at the same time. If you wish, you can also use `/` in tag names to create hierarchical tags.

## Generating index

Minimal Mistakes can be indexed based on categories and tags. But this process is not completely automatic. Taking categories as an example, Minimal Mistakes provides a layout called `categories`. Any page using this layout will automatically display all `categories` and the posts they contain. However, pages using this layout are not automatically created. You need to create a page yourself and then set it to use `categories` layout. If you want to implement the function of jumping to the categories index by clicking on its category on the post page, you also need to set the `permalink` of the index page to `/categories/`. It should be noted that the index page of categories itself is considered a page, not a post. So please put it in the website root directory or `_pages`.

Minimal Mistakes also gives an example of a `category-archive.md` file: <https://github.com/mmistakes/minimal-mistakes/blob/master/docs/_pages/category-archive.md>.

In order to easily check which posts do not have a category set, you can use `defaults` in `_config.yml` to set a default category for all posts (for example `Uncategorized`).

Under <https://github.com/mmistakes/minimal-mistakes/tree/master/docs/_pages> you can also find some other examples, such as `tag-archive` for tags index, `year-archive` for years index.

It is important to note that these indexes are only effective for posts. If you want to perform similar indexes on other pages, you can use Liquid to implement it yourself.
