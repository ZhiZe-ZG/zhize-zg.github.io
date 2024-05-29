---
title: "Software Research Introduction"
permalink: /SoftwareResearch/Introduction
date: 2024-03-13 18:44:51 +0800
category: SoftwareResearch
tags:
header:
  teaser: https://upload.wikimedia.org/wikipedia/commons/1/14/Window_%28windowing_system%29.svg
---

This is the introduction to the series articles "Software Research". This series introduces basic information about the software that I am concerned about.

## Main Categories of "Software"

This series mainly introduces application software. Application software refers to software that is used directly by people to fulfill a certain need. Operating systems and hardware drivers are not included.

Network services are not application software. The gray area here is the use of network services. Some software act as a network service client. The following provisions are made here:

* Client software dedicated to a certain commercial network service is regarded as an accessory to the network service and is not regarded as an application software.
* Software that is not targeted at a specific network service provider, but serves as a client for a type of network service protocol, is an application software (such as an e-mail client).

## Extensions and Libraries

For frequently used software, if it has extendsions, the extended software should also be researched and managed. Create a folder with the same name for the software and record the posts about extensions in it.

If the extendsions of multiple software are universal, this should be stated in the descriptions of these software, and the extendsions library of one software should be designated as priority. Generally speaking, extendsions supported by several mutually compatible software are recorded only once.

In addition, relatively fixed and systematic configurations or settings can also be counted as extendsions. For program development environments, all libraries count as extensions. When the programming language runtime environment and the package manager in the development environment are not the same software, all libraries are recorded under the package manager.

In fact, the application softwares themselves are also regarded as extensions of the operating system. What manages them is the system's package management software.

## About Package Dependency

Software that is not used directly used by human and is simply a dependency of other software is generally not recorded. So as the runtime environments of some languages. These softwares should be automatically installed and managed by package management software. If necessary, mention the need to install them in the introductions of the relevant application softwares.

But the libraries called in the programming environment need to be recorded. Because calling them is equivalent to using them directly.

## About Game DLCs and Mods

Game DLC and Mods are managed by add-on packs for the game. But a mere game track is essentially a record sale, and it doesn't fall into this category. In addition, merely selling virtual items without altering the game's data also does not count.

## Symbols and Tags

Here are descriptions of the symbols I'll use in the articles:

* Openness
  * Open Source?
    * 📖 Open Source
    * 📕 Close Source
  * Charge?
    * 🆓 Free
    * 💰 Charge
* System
  * Developer System
    * 🪟 Windows
    * 🍎 MacOS
    * 🐧 Linux-bsed
    * 😈 BSD-based
  * Consumer System
    * 🍏 Apple consumer systems (iOS, iPadOS etc.)
    * 🤖 Android-based consumer systems

Here are some tags I would label these articles:

* Basic Interface
  * CLI: Command Line Interface. Mainly interact with text commands. Can be run in a virtual terminal, but may also be run in other ways such as voice interaction. After all, text commands are abstract and can be used in various carrier.
  * TUI: Text-based User Interface. An interface with a graphical layout rendered in a terminal.
  * GUI: Graphical User Interface. A true flat graphical interface, with keyboard and pointing device as the main control method.
  * TouchGUI: Graphical User Interface. Finger touch is the main mode of operation.

In addition, I will add at least one tag describing the functional positioning of each software. The number of such tags is variable.

## Recommended Softwares

Here are some softwares I recommend personally.

* [Recommended Softwares](/SoftwareResearch/RecommendedSoftwares)
