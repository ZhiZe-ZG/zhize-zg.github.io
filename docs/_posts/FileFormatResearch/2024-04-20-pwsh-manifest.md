---
title: "PowerShell Manifest"
date: 2024-04-20 21:30:05 +0800
category: FileFormatResearch
tags: Text-File Shell-Script
header:
  teaser: https://upload.wikimedia.org/wikipedia/commons/a/af/PowerShell_Core_6.0_icon.png
---

## Basic Information

Parent Format: Plain Text File

MIME Name: text/powershell-manifest (non-standard)

Suffix： `.psd1`

Openness: 🆓📖

Related Sites:

* [Microsoft Build: PowerShell - Modules](https://learn.microsoft.com/en-us/powershell/scripting/lang-spec/chapter-11?view=powershell-7.4)
* [Microsoft Build: PowerShell - New-ModuleManifest](https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.core/new-modulemanifest?view=powershell-7.4)

## Introduction

PowerShell manifest is a file that defines a PowerShell module. It is different from PowerShell module file. PowerShell module file directly exports externally accessible objects. Manifest returns a hashtable. In addition to defining exported objects, this hashtable can also define information such as module version.
