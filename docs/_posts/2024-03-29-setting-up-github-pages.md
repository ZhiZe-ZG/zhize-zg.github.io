---
title:  "Setting Up GitHub Pages"
date:   2024-03-29 15:16:36 +0800
---

GitHub Pages is a free personal website hosting provided by GitHub. You can use this service to build your own website for resumes, project presentations, blogs or online documents.

Specifically, users upload website content to GitHub in the form of GitHub repository, and then GitHub applies templates based on these contents to automatically generate website files and deploy them on the server provided by GitHub. Many of the details can be customized, but GitHub supports generating websites based on Jekyll by default. The generated website can be accessed directly on the Internet, and the default address is `<user-name>.github.io`. The `<user-name>` represents your GitHub account username. This name is set during registration and exists in the links to your GitHub repositories.

If you want to set up your own GitHub Pages, there is a detailed  official documentation available:

* [GitHub Pages documentation](https://docs.github.com/en/pages)

But for me the documentation is not very satisfying. Therefore, I will organize and supplement what I think is important information in this article.

Let's start with some basics. Simply put, a website is a program running on a server. When a client accesses the website, the program on the server sends the web page data to the client. So, usually we need a server to start website construction. But the basis of the GitHub Pages service is to use GitHub's server as a server for our website. So the server problem is solved.

After having the hardware, we also face the problem of software. We need a program that listens to network requests and delivers web page data when clients accesses the website.



* [Jekyll](https://jekyllrb.com/)
* [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/)

<!--To Be Continue-->



