---
title: "Post Categories and Tags"
date: 2024-03-31 01:34:29 +0800
category: Tech_Note/Personal_Website
tags: GitHub_Pages Jekyll Front_Matter Minimal_Mistakes
---

In this post, we will discuss taxonomy of posts. Jekyll provides two default Front Matter variables for taxonomy of posts. Categoties are used to build tree-like taxonomy, while Tags are used to build multiple-label taxonomy.

The following official documents are for reference:

* [Front Matter - Predefined Variables for Posts](https://jekyllrb.com/docs/front-matter/#predefined-global-variables)
* [Minimal Mistakes Configuration - Archive Settings](https://mmistakes.github.io/minimal-mistakes/docs/configuration/#archive-settings)

## Categories

Jekyll provides two variable names for category taxonomy: `categories` and `category`. Only use the singular form for personal recommendations. In the plural version, multiple category names are not in a parallel relationship but in a hierarchical relationship. But when using the categories archive function of Minimal Mistakes, this hierarchical relationship will not be reflected.

Spaces in `category` are considered separators for different `category` values. If you want to use a single `category` to represent a hierarchical relationship, you can use `/` to separate its value. For example:

```yaml
category: Tech_Note/Personal_Website
```

It should be noted that `category` will change the access path of the page. By default, Jekyll sets the access path of posts to include the writing time and title of the file (Minimal Mistakes omits the writing time by default). When `category` is specified, the post access path consists of `category` and the title in the file name. In addition, if both `category` and `permalink` exist in Front Matter, the access path of the post is determined by `permalink`.

For example, the access path to this post is:

```url
https://www.zhize.xyz/tech_note/personal_website/post-categories-and-tags/
```

`https://www.zhize.xyz` is my website address.

The file name of this post is `2024-03-31-post-categories-and-tags.md`.

The Front Matter of this post is as follows:

```markdown
---
title: "Post Categories and Tags"
date: 2024-03-31 01:34:29 +0800
category: Tech_Note/Personal_Website
tags: GitHub_Pages Jekyll Front_Matter Minimal_Mistakes
---
```

## Tags

If we use an analogy in object-oriented terms, the taxonomy provided by categories are similar to single inheritance of classes, while the taxonomy provided by tags are similar to multiple inheritance of interfaces.

The variable name of Tags is `tags`. Spaces are used to separate multiple different tags. Since tags do not change the access address of the post, a post can have multiple tags at the same time. If you wish, you can also use `/` in tag names to create hierarchical tags.

## Generating index

Minimal Mistakes can be indexed based on categories and tags. But this process is not completely automatic. Taking categories as an example, Minimal Mistakes provides a layout called `categories`. Any page using this layout will automatically display all `categories` and the posts they contain. However, pages using this layout are not automatically created. You need to create a page yourself and then set it to use `categories` layout. If you want to implement the function of jumping to the categories index by clicking on its category on the post page, you also need to set the `permalink` of the index page to `/categories/`. It should be noted that the index page of categories itself is considered a page, not a post. So please put it in the website root directory or `_pages`.

Minimal Mistakes also gives an example of a `category-archive.md` file: <https://github.com/mmistakes/minimal-mistakes/blob/master/docs/_pages/category-archive.md>.

Under <https://github.com/mmistakes/minimal-mistakes/tree/master/docs/_pages> you can also find some other examples, such as `tag-archive` for tags index, `year-archive` for years index.

It is important to note that these indexes are only effective for posts. If you want to perform similar indexes on other pages, you can use Liquid to implement it yourself.

后续再讲

category tags

category 对于路径的影响小于 permalink 但是高于其他

其他的分类不会自动按照 category 或者 tag 分类
但是如果有兴趣可以自己写


tags 也可以分层

<!-- Front Matter 可以保存元数据，使用 Liquid 访问-->
<!--Categories and Tags-->
<!--目录和标签的逻辑分类-->
<!--目录会影响 post 路径，没有目录的文章路径-->
<!--目录建议用一个，用分隔划分层次，方便生成索引-->
<!--标签很多个-->
<!--索引生成->
<!--Liquid 的简单语法和 Front Matter 定义元数据-->
<!--To Be Continue-->
<!--更多约定还是参考 Jekyll-->
<!--Jekyll 使用这些自动分类，但是 Minimal Mistake 不是-->
<!--front 信息-->
<!--defaults 信息-->
<!--title 覆盖文件名，路径问题，起名建议-->
<!--分类管理建议-->
<!--pages 的处理方式-->
<!--其他类别，例如写一本书，就可以建立一个新的类别-->
<!--使用初始化工具可以，但是理解每一行配置更重要，所以一行一行抄也是一个办法-->
<!--Collection, pages 不是 collection， collection 也不用加 include， 自带的 collection 有 posts，pages 和 drafts ， pages 一般没有专门路径但是 Minimal Mistakes 需要设置，这个不说也行-->
<!--Collection 的索引-->
https://jekyll-one-org.github.io/pages/public/learn/bookshelf/jekyll_collections/
https://jekyllrb.com/docs/collections/