---
title: "Run Command as Administrator in PowerShell on Windows"
date: 2024-04-01 22:48:10 +0800
category: Tech-Note/Using-Windows
tags: Windows PowerShell WindowsTerminal
---

When configuring and using a personal computer, it is necessary to obtain administrator rights. On Windows systems, the option to run as administrator can be found in the right-click menu (or shift right-click menu). This is not friendly to virtual terminal users.

Recently I stumbled upon a way to launch a program with administrator rights from the command line. It's rather simple, like this:

```powershell
Start-Process pwsh -Verb RunAs
```

The `Start-Process` is a PowerShell Command to start a new proces. Put the name or path of the program you want to start after it. Here `pwsh` is the command to start PowerShell. Note that the `powershell` is the command for Windows PowerShell which is a special old version PowerShell embeded in Windows. The `-Verb RunAs` is the key point which means run the program as an administrator.

`pwsh` will start PowerShell with its own virtual terminal which is very awful to use. If you want to start your beloved terminal, you can replace the `pwsh` with your terminal, like this:

```powershell
Start-Process alacritty -Verb RunAs
```

If you use Windows Terminal, the command to launch it is `wt`. So you can use:

```powershell
Start-Process wt -Verb RunAs
```

I learned this trick from a [Stack Overflow post](https://stackoverflow.com/questions/7690994/running-a-command-as-administrator-using-powershell). I searched the powershell documentation, but the [relevant page](https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.management/start-process?view=powershell-7.4) lacked explanation for `RunAs`. I guess this parameter is related to the old cmd command, but I don't know the details.

In a process without administrator rights, starting the program through this method will still pop up a dialog box requesting administrator rights. This is terrible, but I haven't found a better way yet. I hope Windows will soon add a password verification mechanism like Linux, instead of the stupid mouse clicking dialog box.

Additionally, when you use the `Start-Process` command on a non-Windows system, the `-Verb` parameter is not available.

If you know of a better way to start a process with administrator rights on a Windows system, or have additional information about this topic, please let me know via e-mail.
