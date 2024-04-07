---
title: "PowerShell"
date: 2024-03-15 10:45:00 +0800
category: SoftwareResearch
tags: Command-Line-Shell CLI PowerShell
header:
  teaser: https://raw.githubusercontent.com/PowerShell/PowerShell/master/assets/ps_black_64.svg
---

## Basic Information

System: 🪟🍎🐧

Openness: 🆓📖

Related Sites:

* [GitHub: PowerShell](https://github.com/PowerShell/PowerShell)
* [PowerShell Gallery](https://www.powershellgallery.com/)

## Introduction

A shell developed by Microsoft based on .NET. Although primarily used on Windows it can be used on other operating systems as well. Provides a relatively unified built-in command style and a better scripting experience. The overall design idea is to use the transmission of structured data objects to replace the text transmission of the previous shell. These features also affect the performance of PowerShell to a certain extent, so that in some scenarios it is criticized for being too slow to start and consuming too many resources.

PowerShell can use packages from a variety of sources. It itself uses PowerShellGet as PackageProvider and PSGallery as PackageSource. At the same time, it can also call the dotnet package on NuGet, but you need to install the corresponding PackageProvider first. In PowerShell, NuGet's PackageProvider and PackageSource are both called "NuGet". In addition, PowerShell can also use some other PackageProvider or PackageSource.

But when recording packages, only PSGallery packages are recorded. NuGet packages are documented by dotnet.

Windows systems integrate an older version of PowerShell called "Windows PowerShell". It does not affect new versions of PowerShell. Generally speaking, just ignore it.
