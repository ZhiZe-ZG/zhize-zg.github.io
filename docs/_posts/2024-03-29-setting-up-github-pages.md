---
title:  "Setting Up GitHub Pages"
date:   2024-03-29 15:16:36 +0800
---

GitHub Pages is a free personal website hosting provided by GitHub. You can use this service to build your own website for resumes, project presentations, blogs or online documents.

Specifically, users upload website content to GitHub in the form of GitHub repository, and then GitHub applies templates based on these contents to automatically generate website files and deploy them on the server provided by GitHub. Many of the details can be customized, but GitHub supports generating websites based on Jekyll by default. The generated website can be accessed directly on the Internet, and the default address is `<user-name>.github.io`. The `<user-name>` represents your GitHub account username. This name is set during registration and exists in the links to your GitHub repositories.

If you want to set up your own GitHub Pages, there is a detailed  official documentation available:

* [GitHub Pages documentation](https://docs.github.com/en/pages)

But for me the documentation is not very satisfying. Therefore, I will organize and supplement what I think is important information in this article.

## Basic Introduction

Let's start with some basics. Simply put, a website is a program running on a server. When a client accesses the website, the program on the server sends the web page data to the client. So, usually we need a server to start website construction. But the basis of the GitHub Pages service is to use GitHub's server as a server for our website. So the server problem is solved.

After having the hardware, we also face the problem of software. We need a program that listens to network requests and delivers web page data when clients accesses the website. In the era when network technology was just emerging, these softwares certainly needed to be written by website builders themselves. But now there are a large number of website programs available for us to use directly. We can directly use these ready-made software, set it up to realize the website we want and fill it with the content we want to display.

Jekyll is one of such softwares. We only need to write the configuration and content files according to the Jekyll protocol, and then use Jekyll to build the website files. However, the website is not online yet at this time, and we still need to deploy the generated website files on the server to access it on the Internet. GitHub did a lot of work for us in this process. Its Jekyll environment is pre-deployed on the server and can automatically build and deploy the website after we upload the configuration and content files. So all we have left is to write the configuration and content files and upload them.

There are two points that need additional explanation:

1. Although GitHub Pages provides Jekyll build and deployment services by default, you can also customize the build and deployment process. The building and deployment of GitHub Pages is based on GitHub Actions, so customizing this process is actually customizing GitHub Actions.
2. For simple small websites, the configuration of Jekyll is not complicated. But when you want to implement more functions, the development of configurations becomes more complicated. One solution is to modify or re-develop based on the already developed configuration. In Jekyll, the finished configuration for people to call is called "theme". For most GitHub Pages users, choosing and fine-tuning a theme is also an important part of building a website.

<!--To Be Continue-->
## Create GitHub Pages
<!--仓库的搭建不讲，说一下可以直接把仓库作为站点，也可以创建一个文件夹，嵌入其中更推荐后者-->
<!--使用初始化工具可以，但是理解每一行配置更重要，所以一行一行抄也是一个办法-->
* [Jekyll](https://jekyllrb.com/)

## Local Debugging

## Domain Problem
<!--默认域名，域名的购买，设置-->

## Use Themes

* [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/)



