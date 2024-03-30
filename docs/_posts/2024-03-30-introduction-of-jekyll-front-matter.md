---
title: "Introduction of Jekyll Front Matter"
date: 2024-03-30 23:38:53 +0800
category: Tech_Note/Personal_Website
tags: GitHub_Pages Jekyll Front_Matter
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
category: Tech_Note/Personal_Website
tags: GitHub_Pages Jekyll Front_Matter
published: false
---
```

This is a Jekyll predefined global variable that can be used to hide unfinished pages.

## Title

title > <name>

`#` is in the page 不会影响其他页面生成的文章列表等

不是预定义变量，但是使用非常普遍

## 写作时间

和文件名可以不一样，用于分类或者排序，覆盖文件名

## permalink

## layout

## defaults settings in _config.yml

## 分类用数据

后续再讲

category tags

category 对于路径的影响小于 permalink 但是高于其他

<!--Front Matter 简介-->
<!--可以保存元数据，使用 Liquid 访问-->
<!--使用defaults 自动填写-->
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