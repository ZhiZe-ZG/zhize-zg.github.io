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