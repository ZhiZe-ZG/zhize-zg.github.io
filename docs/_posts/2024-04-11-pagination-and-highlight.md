---
title: "Pagination and Code Highlight"
date: 2024-04-11 22:53:59 +0800
category: Tech-Note/Personal-Website
tags: Jekyll Minimal-Mistakes
header:
  teaser: https://upload.wikimedia.org/wikipedia/commons/d/d1/Sanzio_01_cropped.png
---

In the past few days, I have been mainly writing about file format research and software research. However, some adjustments have been made to the website.

## About Collection

Jekyll's collection is a system separate from post and cannot use categories or tags. And the pagination that comes with Jekyll does not search pages in collections by default.

So I rethought my original usage strategy. Although there are generally no changes to the usage strategy, I feel that many functions implemented by collections can actually be implemented using the categories of posts. If you need to organize posts' source code files, just create subfolders directly in `_post`. Jekyll will recursively search the subfolders of `_posts`.

## Pagination

Minimal Mistakes will automatically add a column for recent articles at the bottom of the home layout. If the pagination function is not enabled, all your posts will be listed here at once. After enabling paginations, multiple versions of your homepage will be automatically generated. The default homepage only has the most recent articles. When you click the page number buttons, you will jump to other versions of the homepage. The other content of these homepages is the same as the default homepage, but older posts will be displayed at the bottom.

It should be noted that if you want pagination to take effect, your homepage cannot use `index.md`. Only `index.html` works. This should be an implementation problem.

The pagination function is provided by Jekyll. You can write Liquid codes to use this function on other pages, refer to:

* [Jekyll DOCS: Pagination](https://jekyllrb.com/docs/pagination/)

## Code Highlight

Jekyll provide code highlighting with [rouge](https://github.com/rouge-ruby/rouge). So, if you use the code highlighting, check the support list of rogue:

* [List of supported languages and lexers](https://github.com/rouge-ruby/rouge/wiki/List-of-supported-languages-and-lexers)

Also refer to:

* [Jekyll DOCS: Tags Filters - Code snippet highlighting](https://jekyllrb.com/docs/liquid/tags/#code-snippet-highlighting)

There are some differences between highlighters. For example, both `powershell` and `pwsh` can refer to PowerShell in VS Code but rogue only support `powershell`. 
