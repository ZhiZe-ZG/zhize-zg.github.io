---
title:  "Setting Up Jekyll for Develop GitHub Pages"
date:   2024-03-30 13:42:04 +0800
category: Tech-Note/Personal-Website
tags: GitHub-Pages Ruby Jekyll Bundler Minimal-Mistakes
header:
  teaser: https://pages.github.com/images/slideshow/jekyllrb.png
---

In this post, we will talk about how to set up a local Jekyll environment to  test your site before upload to GitHub Pages. Then we will introduce Minimal Mistakes, a famous Jekyll theme for personal website. Hope you have already known how to deploy a basic GitHub Pages site before reading this.

The following official sites are for reference:

* [Ruby](https://www.ruby-lang.org/en/)
* [Jekyll](https://jekyllrb.com/)
* [Bundler](https://bundler.io/)
* [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/)

## Local Ruby Environment

Every time you upload your site repository to GitHub, GitHub will regenerate and update your site. But the build time of several minutes each time makes debugging troublesome. Therefore, we need a local environment to finish debugging before upload. The local Jekyll environment can preview most page updates in real time. To preview settings updates for the entire website, you only need to restart the local website process.

The Jekyll is write in Ruby, so you need first install the Ruby environment. On most operating systems, you can just follow the [Official Ruby Install Guide](https://www.ruby-lang.org/en/downloads/). If  you use Windows, in addition to manually downloading the installation package, you can also use winget to automatically complete the installation. For example:

```powershell
winget install --id RubyInstallerTeam.RubyWithDevKit.3.2
```

It is recommended to install a version with MSYS2 (these versions' IDs contain `WithDevKit`). MSYS2 offers a series Linux tools ported to Windows. They are the elemental support of most the Ruby-related softwares.

Gem is a package management tool in Ruby develop environment. You can use it update your Ruby environment:

```powershell
gem update --system
```

Then install Jekyll with it:

```powershell
gem install jekyll
```

The functions provided by Gem are relatively basic, so in actual development, people generally use bundler to manage dependencies for each Ruby project. Therefore, next we install bundler using Gem.

```powershell
gem install bundler
```

It should be noted that the bundler command is `bundle` without `r`.

## Local Debugging

Before start local Jekyll process, we should install all the dependencies with bundler. The bundler need a `Gemfile` to start with. If you follow the GitHub Pages quickstart guide. You may not have created a `Gemfile` yet. So we create a new Jekyll project and copy the `Gemfile` into our project. To create a new Jekyll project, you need these commands:

```powershell
New-Item new_site
Set-Location new_site
jekyll new .
```

`Gemfile` specifies the packages required by our website. You can modify it as needed. The automatically generated `Gemfile` just gives us a convenient starting point.

In the `Gemfile` this line specifies where to download packages:

```gemfile
source "https://rubygems.org"
```

On my Windows system, when running Jekyll I get an error message saying `webrick` is missing. So adding this line to the `Gemfile` fixes the issue:

```gemfile
gem "webrick"
```

Save your `Gemfile` and execute bundler in the path containing `Gemfile` to complete the installation of dependencies:

```powershell
bundle install
bundle update
```

It should be noted that the folder where `Gemfile` is stored is generally the folder where our website’s configuration file `_config.yml` and the main page file `index.md` are stored.

Then use this command to launch your web site:

```powershell
bundle exec jekyll serve
```

If the command successfully starts the web page process, you will see your local website access address in the command line prompt like this:

```text
Server address: http://127.0.0.1:4000
```

At this point you can use your browser to access the website running on your local computer. Your changes to ordinary page content will be updated on the local website in real time.

## Using Theme

A Jekyll theme is a collection of Jekyll configuration files and web page style files. GitHub Pages comes with several simple themes but the functionality of these themes is too thin. So I recommend using some of the more polished and full-featured themes. There is no need to repeat development when we need some website functions.

I personally use the Minimal Mistakes theme, and the following introduction will also use this as an example.

You can complete the installation of Minimal Mistakes according to [Minimal Mistakes Quick-Start Guide](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/). The process is basically to add some items to the `Gemfile` and `_config.yml` and then use bundler to install them automatically. If your website doesn’t have a lot of configuration, I recommend just copying the `_config.yml` of Minimal Mistakes and filling in your own information.

Finally, you can create a very simple home page with the following code in `index.md`:

```markdown
---
layout: home
title: ZhiZe' GitHub Pages
---

Some tech essays of ZhiZe.
```

Remember to replace the title and web page content ("Some tech essays of ZhiZe.") with your own.

## Update 2024-08-16

The old install method is not working well. Follow the Jekyll official install instruction:

* [Jekyll - Quickstart](https://jekyllrb.com/docs/)

Remamber to install the requirements first.

To avoid path and right error, set the install path for gem like this:

```bash
# gem
export PATH=$PATH':$HOME/.gem'
export GEM_HOME=$HOME/.gem
export GEM_PATH=$HOME/.gem
```

or like this in PowerSHell:

```powershell
# gem
$env:Path += ";$HOME/.gem"
$env:GEM_HOME = "$HOME/.gem"
$env:GEM_PATH = "$HOME/.gem"
```
