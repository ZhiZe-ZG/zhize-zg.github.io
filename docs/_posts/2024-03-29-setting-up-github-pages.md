---
title:  "Setting Up GitHub Pages"
date:   2024-03-29 15:16:36 +0800
category: TechNote
tags: GitHubPages Jekyll NameCheap
---

GitHub Pages is a free personal website hosting provided by GitHub. You can use this service to build your own website for resumes, project presentations, blogs or online documents.

Specifically, users upload website content to GitHub in the form of GitHub repository, and then GitHub applies templates based on these contents to automatically generate website files and deploy them on the server provided by GitHub. Many of the details can be customized, but GitHub supports generating websites based on Jekyll by default. The generated website can be accessed directly on the Internet, and the default address is `<user-name>.github.io`. The `<user-name>` represents your GitHub account username. This name is set during registration and exists in the links to your GitHub repositories.

If you want to set up your own GitHub Pages, there is a detailed  official documentation available:

* [GitHub Pages documentation](https://docs.github.com/en/pages)

But for me the documentation is not very satisfying. Therefore, I will organize and supplement what I think is important information in this article.

Please note that: **This article is intended primarily as an introduction and supplement to documents. If you have any questions while reading, please refer to the documents listed in this article.**

## Basic Introduction

Let's start with some basics. Simply put, a website is a program running on a server. When a client accesses the website, the program on the server sends the web page data to the client. So, usually we need a server to start website construction. But the basis of the GitHub Pages service is to use GitHub's server as a server for our website. So the server problem is solved.

After having the hardware, we also face the problem of software. We need a program that listens to network requests and delivers web page data when clients accesses the website. In the era when network technology was just emerging, these softwares certainly needed to be written by website builders themselves. But now there are a large number of website programs available for us to use directly. We can directly use these ready-made software, set it up to realize the website we want and fill it with the content we want to display.

Jekyll is one of such softwares. We only need to write the configuration and content files according to the Jekyll protocol, and then use Jekyll to build the website files. However, the website is not online yet at this time, and we still need to deploy the generated website files on the server to access it on the Internet. GitHub did a lot of work for us in this process. Its Jekyll environment is pre-deployed on the server and can automatically build and deploy the website after we upload the configuration and content files. So all we have left is to write the configuration and content files and upload them.

There are two points that need additional explanation:

1. Although GitHub Pages provides Jekyll build and deployment services by default, you can also customize the build and deployment process. The building and deployment of GitHub Pages is based on GitHub Actions, so customizing this process is actually customizing GitHub Actions.
2. For simple small websites, the configuration of Jekyll is not complicated. But when you want to implement more functions, the development of configurations becomes more complicated. One solution is to modify or re-develop based on the already developed configuration. In Jekyll, the finished configuration for people to call is called "theme". For most GitHub Pages users, choosing and fine-tuning a theme is also an important part of building a website.

## Create GitHub Pages

The GitHub Pages service is based on GitHub repositories. The configuration and content files used to generate the GitHub Pages site need to be uploaded to a GitHub repository. Each GitHub account can have multiple GitHub repositories, but only one GitHub Pages site. Therefore, the general approach is to create a repository specifically for GitHub Pages and store all configuration and content files in it.

After my personal testing, the name of the repository is not important, but the repository is generally named `<user-name>.github.io` (the `<user-name>` represents your GitHub account username). The content related to repository creation and git usage will not be discussed here.

After the repository is built, follow steps in [Creating a GitHub Pages site](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site) to complete the settings to construct GitHub Pages site.

In settings, you can directly use the repository root directory to store website configuration and content files. But I prefer to use the `docs` folder in the root directory to store this content. Because it facilitates management. In other folders under the root directory, you can store description files or automated scripts related to website construction that you do not want to display directly on the website.

To verify that the website is running successfully, you can try accessing `<user-name>.github.io` in your browser. There are many reasons why this URL cannot be accessed normally. Here is a special mention of the issue of no default homepage. According to Jekyll's convention, `index.md` or `index.html` under the website file path (root directory or `docs`) will be recognized as the website homepage. If the file does not exist or is blank, the displayed home page may also be blank. At this point the website is running normally, but the homepage looks unresponsive. So please make sure you write some displayable content in `index.md` or `index.html` to facilitate testing the website status. 

For other settings, please refer to the documentation or tutorials. These should be kept as simple as possible, just enough to make sure the website works. Please wait until the website can run normally before trying to organize or standardize them.

## Domain Problem





<!--To Be Continue-->
<!--index.md 或者 index.html 比 README 更优先，确保有一个可以看到的内容以测试网站是否成功运行。更多约定还是参考 Jekyll-->
<!--使用初始化工具可以，但是理解每一行配置更重要，所以一行一行抄也是一个办法-->

* [Jekyll](https://jekyllrb.com/)

<!--默认域名，域名的购买，设置-->

## Local Debugging

## Use Themes

* [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/)



