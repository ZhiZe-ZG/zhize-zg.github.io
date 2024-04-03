---
title: "Skills For Deeper Jekyll Usage"
date: 2024-04-03 01:37:56 +0800
category: Tech-Note/Personal-Website
tags: GitHub-Pages Jekyll Markdown HTML Liquid Front-Matter YAML CSS SCSS Sass JavaScript CoffeeScript Ruby
header:
  teaser: https://upload.wikimedia.org/wikipedia/commons/e/ef/Programming_code.jpg
---

In this posts we'll talk about some skills you need to learn to use Jekyll in depth.

## Markdown and HTML

Markdown is a simple markup language for writing documents. Most of the previously mentioned pages are written in Markdown. It is essentially a simplification of part of the syntax of HTML. The source code of documents written in Markdown is generally more concise and more readable than HTML, but when you want to define complex layout, you still need to embed HTML code in Markdown or use HTML format directly.

In order to combine the advantages of HTML and Markdown, we can use HTML to define the layout, and then use Markdown to write the article content with the layout.

Jekyll's layout files are stored in `_layouts`. If your layouts can be split into many components, you can write these components into separate HTML files and place them in `_includes`. Reference these `_includes` in your layout definitions when needed. For more information about these two folders, please refer to:

* [Jekyll DOCS: Layouts](https://jekyllrb.com/docs/layouts/)
* [Jekyll DOCS: Includes](https://jekyllrb.com/docs/includes/)

## CSS

In the current web page framework, HTML, CSS and JavaScript respectively define part of the information of the web page.

HTML mainly defines the layout structure and static content of web pages. CSS defines the specific display styles of the structures defined in HTML. For example, you can define in HTML which paragraph is the title, which paragraph is the body text, and which paragraph is the quote. But the fonts, font sizes and colors used for titles, body text and quotes are defined by CSS. The reason why structure and style should be expressed in HTML and CSS respectively is not because HTML does not have the ability to express styles. This is to facilitate the management and maintenance of website projects.

So if you want to make your website look more customized, knowing some CSS syntax is also a must.

## JavaScript

JavaScript is used to define behavior. The so-called "behavior" is a relatively abstract concept. In a general tutorial, an example would be as follows: if you want a web page to display different content based on the current date or if you want to add an interactive button for users to click, you need JavaScript. But these examples are actually problematic. Because you can also do something similar by generating a large number of static pages that link to each other.

To understand the usefulness of JavaScript, we need to understand what "behavior" is and how these behaviors occur. Generally speaking, content like HTML or CSS is called "data", and any modifications made to the data are called "behavior".

There are many behaviors involved in the creation and browsing of web pages. Manually writing HTML is human behavior, and in addition, computers automatically do some behavior to web page files. Computer behavior may occur on any computer involved in the delivery or display of web pages. For examples, a static page is automatically generated through a program before the website is built, the web page content is modified before the server sends the web page, and the web page file is modified again by the user's browser after receiving the web page file. These are all computer behaviors.

The JavaScript files delivered with the HTML files can only control the modification behavior of the user's browser to the HTML. Modifications to web page files on the server and earlier modifications cannot be processed by these JavaScript files. Still, JavaScript running in the browser can already do a lot. If you want your web pages to adjust in the user's browser or want to add some animation or interactive features, it is recommended to learn some JavaScript. But if you just need a static display page, JavaScript is not particularly needed.

## Liquid

Liquid is a markup language embedded in HTML. It also controls behavior in a broad sense. However, the behavior controlled by Liquid does not occur in the browser, nor on the website server that deliveres the HTML file, but occurs during the construction of the website file.

Taking GitHub Pages as an example, the HTML you write with Liquid marks is uploaded to GitHub along with the repository. At this time, your GitHub Pages will not be refreshed immediately. Instead, other GitHub servers will first run Jekyll to process your website files and translate the Liquid paragraphs into pure HTML. Only the translated pure HTML will be updated to your GitHub Pages. Although we use the word "translate" here, in fact Liquid and HTML do not correspond one-to-one. What actually happens is that Jekyll automatically generates HTML paragraphs based on instructions from Liquid.

The basic function of Liquid is to generate some similar HTML paragraphs, reducing the stress of writing repetitive HTML. On this basis, it also has some simple flow control and data processing functions.

Lquid is the basis for many features of Jekyll. For example, the implementation of the layout function is based on Lquid. You need to use Lquid in the layout file to indicate where the content paragraph extracted from the Markdown file should be placed in the layout template.

To learn more about Liquid, refer to:

* [Liquid Official Site](https://shopify.github.io/liquid/)
* [Jekyll DOCS: Liquid](https://jekyllrb.com/docs/liquid/)

## Front Matter and YAML

We introduced the concept of "metadata" before. Simply put, "metadata" is data that is not necessarily directly displayed on the web page but has an impact on the final display content and effect of the web page.

Liquid is not good at data representation, so Jeykll introduced Front Matter to define metadata for pages. The so-called Front Matter is a small piece of YAML at the beginning of the file. YAML is a data representation language. That means TAML is specifically designed to represent data. In addition to Front Matter, which is used to represent page metadata, Jekyll's configuration file `_config.yml` is also written in YAML.

Jekyll provides a mechanism that allows Liquid to directly access data defined by Front Matter or data automatically provided by some Jekyll systems. Therefore, to use Liquid well, it is necessary to understand Front Matter and YAML.

Here are some references on Front Matter, YAML or configurations about Jekyll and Minimal Mistakes:

* [Jekyll DOCS: Front Matter](https://jekyllrb.com/docs/front-matter/)
* [YAML](https://yaml.org/)
* [Jekyll DOCS: Configuration](https://jekyllrb.com/docs/configuration/)
* [Minimal Mistakes: Configuration](https://mmistakes.github.io/minimal-mistakes/docs/configuration/)

## SCSS, Sass and CoffeeScript

Just like the Liquid for generating HTML, there is SCSS (and Sass) for CSS and CoffeeScript for JavaScript. SCSS is a language for generating CSS that simplifies writing CSS. Sass offers similar functionality, but with a different level of simplicity. CoffeeScript is a language that generates JavaScript to simplify the work of writing JavaScript.

Strictly speaking, the function provided by Liquid is called template generation, while SCSS, Sass and CoffeeScript are more like languages that need to be compiled. There are certain differences between the two, but we will not go into details here.

Jekyll supports these languages and provides a concise guide:

* [Jekyll DOCS: Assets](https://jekyllrb.com/docs/assets/)

To learn more about them, refer to:

* [Sass Official Site](https://sass-lang.com/)
* [CoffeeScript Official Site](https://coffeescript.org/)

## Data Files and Static Files

HTML is text-centric, so some non-text data is difficult to place directly in HTML. All HTML can do is leave display space for them and then reference them. Jekyll call them "static files". Image files are typical static files. You can directly place the static files in the specified path of the website files and reference them in the HTML. Jekyll also has a guide for static files:

* [Jekyll DOCS: Static Files](https://jekyllrb.com/docs/static-files/)

Due to the limited capacity of the GitHub repository, I do not recommend that you store too many static files in your website project. A few frequently used static files such as website logos and personal avatars can be placed in website projects. As for the accompanying pictures or decorative background pictures for each page, it is better to upload them to the image hosting services and then quote them.

In addition, HTML's grammatical design focuses more on web page layout than general data representation. Therefore, although some data can be represented in text, writing it in HTML syntax will be complex and lengthy. You can write them out using a specialized data representation syntax and store them in the `_data` folder. Use Liquid to access them when you need them. Jekyll also provides a guide for this:

* [Jekyll DOCS: Data Files](https://jekyllrb.com/docs/datafiles/)

## Ruby and Jekyll Plugins

If you think the functionality you need is not provided by Jekyll and cannot be customized through the languages or frameworks introduced above, you can extend the functionality of Jekyll through plug-ins. There are already many Jekyll plug-ins written by others for use. If no one has implemented the function you are looking for, you can also develop it yourself using Ruby.

Here are some documents that may be helpful:

* [Jekyll DOCS: Plugins](https://jekyllrb.com/docs/plugins/)
* [Ruby Official Site](https://www.ruby-lang.org/en/)

It should be noted that GitHub Pages only provides limited plugin support. If the plugin function you need is not provided by GitHub Pages and this function is very important to you, then I suggest that you use your own server to build the website instead of using GitHub Pages. Here is a list about plugins that GitHub Pages support:

* [GitHub Pages Documentation: Plugins](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll#plugins)
