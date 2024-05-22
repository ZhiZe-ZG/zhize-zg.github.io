---
title: "Recommended File Format"
permalink: /FileFormatResearch/RecommendedFileFormat
date: 2024-05-22 13:49:10 +0800
category: FileFormatResearch
tags:
header:
  teaser: https://upload.wikimedia.org/wikipedia/commons/b/b0/File-dynamic-color.png
---

## Audio Sampling

* 🆓📖 `.aac` [AAC](/fileformatresearch/2024/05/02/aac): Lossy audio sample format, but better than mp3.
* 🆓📖 `.flac` [FLAC](/fileformatresearch/2024/05/02/flac): Lossless audio sample format.
* 🆓📖 `.mka` [Matroska Audio](/fileformatresearch/2024/05/05/mka): Matroska audio. Used to encapsulate complex audio files or as components of other Matroska formats.

Read only:

* 🆓📖 `.mp3` [MP3](/fileformatresearch/2024/05/02/mp3): Lossy audio sample format.
* 🆓📖 `.wav` [Waveform Audio File Format](/fileformatresearch/2024/05/05/wav): An audio file format. It uses the linear pulse-code modulation (LPCM).

## Archive

### Optical Disc Archive

* 🆓📖 `.iso` [ISO](/fileformatresearch/2024/04/11/iso): An optical disc file system image file format.

### Universal File System Archive

* 🆓📖 `.7z` [7Z](/fileformatresearch/2024/04/10/7z): General archive and compression format with more function and better compression ratio than ZIP. But not many file formats use 7Z as the base format.

Read only:

* 🆓📖 `.bz2` [Bzip2](/fileformatresearch/2024/04/10/bzip2-format): Single file compression format.
* 🆓📖 `.gz` [Gzip](/fileformatresearch/2024/04/10/gzip): Single file compression format.
* 💰📕 `.rar` [RAR](/fileformatresearch/2024/04/10/rar): Archive and compression format.
* 🆓📖 `.tar` [Tar](/fileformatresearch/2024/04/10/tar): Archive file format. One advantage of this format is that Tar can save file permission information on file systems of Unix-like systems. But I personally think it's better to include a shell script with the archive to set the file permissions. This eliminates the need to use a tar archive.
* 🆓📖 `.xz` [XZ](/fileformatresearch/2024/04/10/xz): Single file compression format.
* 🆓📖 `.zip` [ZIP](/fileformatresearch/2024/04/10/zip): General archive and compression format, also as the basis for many other file formats.

## Bibliography Data

* 🆓📖 `.bib` [BibTeX](/fileformatresearch/2024/04/15/bib): A data format for recording citation sources.

## Document Typesetting Description

### Common Document Typesetting Description

* 🆓📖 `.md` [Markdown](/fileformatresearch/2024/04/10/markdown-format): A simple markup format used to write documents without complex style or structure.
* 🆓📖 `.tex` [TeX](/fileformatresearch/2024/04/15/tex): Markup language format for TeX typesetting system.

### Web Page Style Sheet

* 🆓📖 `.css` [Cascading Style Sheets](/fileformatresearch/2024/04/19/css): A markup language used to describe the styles of HTML elements.
* 🆓📖 `.scss` [SCSS](/fileformatresearch/2024/04/19/scss): A markup language that generates CSS. It's like an extension to SCSS.

Read only:

* 🆓📖 `.sass` [Sass](/fileformatresearch/2024/04/19/sass): A markup language that generates CSS.It uses indentation to indicate code levels.

### Web Page Typesetting

* 🆓📖 `.html` [HyperText Markup Language](/fileformatresearch/2024/04/19/html): Markup language for Web typesetting.

## E-document

### Electronic Display

* 🆓📖 `.epub` [EPUB](/fileformatresearch/2024/04/10/epub): E-book format based on web related technologies.

Read only:

* 🆓📕 `.chm` [Microsoft Compiled HTML Help](/fileformatresearch/2024/04/17/chm): Compiled HTML documents.

### Imitating Paper

* 🆓📖 `.pdf` [Portable Document Format](/fileformatresearch/2024/04/09/png): Mainly used as document format for both scanned and rendered, sometimes used as vector image format.

Read only:

* 🆓📖 `.djvu` [DjVu](/fileformatresearch/2024/04/10/djvu): Document format or pixel image format for scanned documents.

### Editable Document Container

* 🆓📖 `.docx` [Office Open XML Document](/fileformatresearch/2024/04/24/docx): Editable document container for Microsoft Office Word etc.

Read only:

* 💰📖 `.doc` [Microsoft Office Word Binary File Format](/fileformatresearch/2024/04/24/doc): Editable document file format.
* 🆓📖 `.odf` [OpenDocument Formula](/fileformatresearch/2024/04/24/odf): A format to save math formula typesetting.
* 🆓📖 `.odt` [OpenDocument Text](/fileformatresearch/2024/04/24/odt): An editable document file container format.

## Hardware and Operating System Level Programming

### C Compiler Source Files

* 🆓📖 `.c` [C Programming Language Source File](/fileformatresearch/2024/05/05/c-source): Source code file format of the C programming language.
* 🆓📖 `.h` [C Programming Language Header File](/fileformatresearch/2024/05/05/c-header): Header file format of the C programming language.

### C++ Compiler Source Files

* 🆓📖 `.cpp` [C++ Programming Language Source File](/fileformatresearch/2024/05/05/cpp-source): Source code file format of the C++ programming language.
* 🆓📖 `.hpp` [C++ Programming Language Header File](/fileformatresearch/2024/05/05/cpp-header): Header file format of the C++ programming language.

### Rust Compiler Source Files

* 🆓📖 `.rs` [Rust Programming Language Source File](/fileformatresearch/2024/05/05/rust-source): Source code file format of the Rust programming language.

## Pixel Image

* 🆓📖 `.apng` [Animated PNG](/fileformatresearch/2024/04/09/apng): Lossless animated pixel image format.
* 🆓📖 `.jpg` [JPEG Format](/fileformatresearch/2024/04/09/jpeg): Lossy pixel image format.
* 🆓📖 `.png` [Portable Network Graphics](/fileformatresearch/2024/04/09/pdf): Lossless pixel image format.

Read only:

* 🆓📖 `.gif` [Graphics Interchange Format](/fileformatresearch/2024/04/09/gif): Lossless animated pixel image format.

## Plain Text

Files without extensions will be treated as plain text files by default. But there is still a suffix for plain text files:

* 🆓📖 `.txt` [Plain Text File](/fileformatresearch/2024/04/07/text-file): Basic text file format.

## System Shell Script

Different shells are essentially different runtime environments, but are grouped together because they serve the same purpose.

### Bash Environment

A type of shell script mainly used on Unix systems (including Bourne Shell). Overall the syntax is archaic and strange. Sometimes adding an extra space before or after an operator can cause errors.

* 🆓📖 `.sh` [Bourne Shell](/fileformatresearch/2024/04/19/sh-format): Universal system management script for Unix.
* 🆓📖 `.profile` [Bourne Shell Config](/fileformatresearch/2024/04/19/sh-config): The file used for the initial configuration of the Bourne Shell. It is also supported by many other shells.
* 🆓📖 `.bashrc` [Bash Config](/fileformatresearch/2024/04/19/bash-config): Script for setting up Bash.

### PowerShell Runtime Environment

* 🆓📖 `.ps1` [PowerShell](/fileformatresearch/2024/04/19/pwsh-format): PowerShell script file.
* 🆓📖 `.psm1` [PowerShell Module](/fileformatresearch/2024/04/20/pwsh-module): PowerShell module file.
* 🆓📖 `.psd1` [PowerShell Manifest](/fileformatresearch/2024/04/20/pwsh-manifest): Manifest for generate PowerShell Module.

## Timed Text

* 🆓📖 `.lrc` [LRC](/fileformatresearch/2024/05/05/lrc): A simple lyric file format. Mainly for music.
* 🆓📖 `.mks` [Matroska Subtitle](/fileformatresearch/2024/05/05/mks): Matroska subtitle. Used to encapsulate complex subtitle files or as components of other Matroska formats.
* 🆓📖 `.srt` [SubRip](/fileformatresearch/2024/05/05/srt): A plain text-based external subtitle format.

## Tabular Data

Tabular data does not necessarily need to be represented in a dedicated tabular file format. It is also possible to use the common markup data format like JSON or XML.

* 🆓📖 `.xlsx` [Office Open XML Workbook](/fileformatresearch/2024/04/28/xlsx): Spreadsheet file format, used for display tables or simple data tables, with some data processing functions.

Read only:

* 🆓📖 `.csv` [Comma-Separated values](/fileformatresearch/2024/04/21/csv): A simple markup language for representing tabular data. Use comma as delimiters. There are some variations of it. They are collectively called "Delimiter-seperated". Delimiter-seperated values are not as good as binary files in terms of compression rate, and are not as good as XML, JSON, etc. in terms of scalability and data type richness.
* 🆓📖 `.ods` [OpenDocument Spreadsheet](/fileformatresearch/2024/04/28/ods): A spreadsheet file format.
* 🆓📖 `.tsv` [Tab-Separated Values](/fileformatresearch/2024/04/21/tsv): A simple markup language for representing tabular data. Use horizontal tabs as delimiters.
* 💰📖 `.xls` [Microsoft Office Excel Binary File Format](/fileformatresearch/2024/04/28/xls): A data sheet file format.

## Universal Markup Data

Although these file formats can theoretically replace each other, their different syntax designs cause them to have different adaptability to different scenarios. Generally, one or more of them are selected according to the needs or framework requirements. So there are multiple alternatives juxtaposed.

* 🆓📖 `.json` [JavaScript Object Notation](/fileformatresearch/2024/04/21/json): A lightweight data markup language.
* 🆓📖 `.toml` [Tom's Obvious Minimal Language](/fileformatresearch/2024/04/21/toml): A simple config file format.
* 🆓📖 `.xml` [Extensible Markup Language](/fileformatresearch/2024/04/09/xml): A common data representation format.
* 🆓📖 `.yml` [YAML](/fileformatresearch/2024/04/19/yaml): An easy-to-read data file format.

## Universal Runtime Environments

### .NET Runtime Environment

* 🆓📖 `.cs` [C# Programming Language Source File](/fileformatresearch/2024/05/05/cs-source): Source code file format of the C# programming language.
* 🆓📖 `.csproj` [C# Project Description File](/fileformatresearch/2024/05/05/cs-project): The description file of C# project.
* 🆓📖 `.fs` [F# Programming Language Source File](/fileformatresearch/2024/05/05/fs-source): Source code file format of the F# programming language.
* 🆓📖 `.fsproj` [F# Project Description File](/fileformatresearch/2024/05/05/fs-project): The description file of F# project.
* 🆓📖 `.sln` [Dotnet Solution File](/fileformatresearch/2024/05/05/sln): The description file of dotnet solution.

### Python Runtime Environment

* 🆓📖 `.py` [Python](/fileformatresearch/2024/04/19/python-source): A general programming language.

## Vector Font

* 🆓📖 `.otc` [PostScript-flavored OpenType Collection](/fileformatresearch/2024/04/14/opentype-collection): Vector font collection file format. Mainly used for GUI operating systems.
* 🆓📖 `.otf` [PostScript-flavored OpenType](/fileformatresearch/2024/04/14/opentype): Vector font file format. Mainly used for GUI operating systems.
* 🆓📖 `.woff2` [WOFF2](/fileformatresearch/2024/04/14/woff2): Vector font file for web.

Read only:

* 🆓📖 `.ttc` [TrueType-flavored OpenType Collection](/fileformatresearch/2024/04/14/truetype-collection): Vector font collection file format.
* 🆓📖 `.ttf` [TrueType-flavored OpenType](/fileformatresearch/2024/04/14/truetype): Vector font file format.
* 🆓📖 `.woff` [WOFF](/fileformatresearch/2024/04/14/woff): Vector font file for web.

## Vector Image

### Chart Drawing

* 💰📕 `.vsdx` [Visio XML Format](/fileformatresearch/2024/04/28/vsdx): A diagram file format based on XML and ZIP.

Read only:

* 🆓📖 `.odg` [OpenDocument Graphics](/fileformatresearch/2024/04/28/odg): A vector image and diagram file format.
* 💰📕 `.vsd` [Microsoft Office Visio Binary File Format](/fileformatresearch/2024/04/28/vsd): A diagram file format.

### Common Vector Image Format

* 🆓📖 `.svg` [Scalable Vector Graphics](/fileformatresearch/2024/04/09/svg): Vector image format.

### Interactive vector animation

* 🆓📖 `.pptx` [Office Open XML Presentation](/fileformatresearch/2024/04/28/pptx): An interactive graphic file format.

Read only:

* 🆓📖 `.odp` [OpenDocument Presentation](/fileformatresearch/2024/04/28/odp): An interactive graphic file format.
* 💰📖 `.ppt` [Microsoft Office PowerPoint Binary File Format](/fileformatresearch/2024/04/28/ppt): An interactive graphic file.

## Video Container

* 🆓📖 `.mkv` [Matroska Video](/fileformatresearch/2024/05/05/mkv): Matroska video. Used to encapsulate complex audiovisual files.
* 🆓📖 `.mp4` [MP4](/fileformatresearch/2024/05/05/mp4): A common audio and video container formats. Used to encapsulate relatively simple audio and video streams.

Read only:

* 🆓📖 `.avi` [Audio Video Interleave](/fileformatresearch/2024/05/05/avi): An audio and video file format dominated by Microsoft.
* 🆓📖 `.flv` [Flash Video](/fileformatresearch/2024/05/05/flv): An audio and video container for Adobe Flash.
