---
title: "File Format Research Introduction"
permalink: /FileFormatResearch/Introduction
date: 2024-04-06 18:41:53 +0800
category: FileFormatResearch
tags:
header:
  teaser: https://upload.wikimedia.org/wikipedia/commons/b/b0/File-dynamic-color.png
---

File Format Research is a series of introductory articles about file formats I care about.

A file format is an specification that can be executed or parsed by the corresponding computing environment when the data is stored in a standardized format. Therefore, on the surface, the file format is only a specification for the format of each data file. In fact, it is also a specification for the corresponding interpreter, compiler or reading and writing tools.

These articles focus on file formats that are parsed directly as a whole by application software and presented to human directly. The format of some files in a multi-file system that do not need to be directly viewed or modified by humans has low priority.

## File Format Names

Each file format has 3 names:

* Media Type Name as the main identifier.
* Natural Language Name is used for the article titles and paragraphs.
* Suffix Name is used to distinguish file types in the file system.

### Media Type Name

Generally, it is filled in according to the Media Type of IANA (Internet Assigned Numbers Authority). Details can be found at:

* [MIME](https://www.iana.org/assignments/media-types/media-types.xhtml)

For those that cannot be found on MIME, I will find names in other websites such as Wikipedia or arrange the names myself. But this should be marked "non-standard".

It is also possible that one file format corresponds to multiple Media Types. In this case, try to keep one or seperate them into different file types.

### Natural Language Name

For convenience of natural language expression, each file format should have a natural language name. If there is a standard for this name, choose the standard. If there is no standard, choose the common name. I will choose a suitable name by yourself sometimes. It will be used as the document title when introducing the file format.

Although this name is mainly used in natural languages, there should be no duplication.

### Suffix Name

The file extension is part of the file name in the file system and is used to identify the file format type. Generally speaking, the file format suffix is located at the end of the file name, starting with a period `.`, followed by letters or numbers.

The suffix name is mainly determined based on the recommendation of the file format standard or standards maintenance organization. If there is no recommendation, it will be generally used name. In these articles, try to ensure that a suffix name belongs to only one file format. If there is a suffix name conflict, the conflict handling method should be stated.

In addition, a file format generally has only one suffix name. When the letters in the suffix name can be uppercase or lowercase, the lowercase form is generally used. When a file format has multiple suffixes, choose the most commonly used or standardized one. It is possible that a file format have multiple suffix names. Generally speaking, a file format can identify its different variants through the meta information inside the file. It is not necessary to distinguish the variant of file format by suffix name, so currently do not give multiple suffix names to a file format. If must, sperate them into different file format types.

The suffix name will also be used as the abbreviation of the file format. When used as a file abbreviation, all capital letters (and without `.`)are used unless otherwise agreed.

## File format type inheritance

There is an inheritance relationship between file formats. All file formats essentially derive from constraints and specifications on binary files.

When file format B inherits A, every qualified B file is required to be a qualified A file. Improved relationships between file formats are not reflected in this description. The two file formats before and after the improvement are considered to be in a parallel relationship.

If a file format inherits directly from the 8-bit binary byte format, enter "Byte" in the "Parent Format" column.

## About Programming-related Languages

Programming languages that have corresponding file formats record corresponding file formats.

Programming languages that do not have corresponding formats are mentioned as language extensions in their main dependent languages and supplemented with reference materials and tags.

Languages that do not have independent file formats or dependent formats such as BNF are not documented in this series of articles.

## Symbols and Tags

Here are descriptions of the symbols I'll use in this series of articles:

* Openness
  * Open Source?
    * 📖 Open format documentation
    * 📕 Private format documentation
  * Charge?
    * 🆓 Free
    * 💰 Charge

I also add at least one tag describing the usage of each format. The number of such tags is variable.

## Recommended File Format

### .NET Runtime Environment

* 🆓📖 `.cs` [C# Programming Language Source File](/fileformatresearch/2024/05/05/cs-source): Source code file format of the C# programming language.
* 🆓📖 `.csproj` [C# Project Description File](/fileformatresearch/2024/05/05/cs-project): The description file of C# project.
* 🆓📖 `.fs` [F# Programming Language Source File](/fileformatresearch/2024/05/05/fs-source): Source code file format of the F# programming language.
* 🆓📖 `.fsproj` [F# Project Description File](/fileformatresearch/2024/05/05/fs-project): The description file of F# project.
* 🆓📖 `.sln` [Dotnet Solution File](/fileformatresearch/2024/05/05/sln): The description file of dotnet solution.

### Audio Sampling

* 🆓📖 `.aac` [AAC](/fileformatresearch/2024/05/02/aac): Lossy audio sample format, but better than mp3.
* 🆓📖 `.flac` [FLAC](/fileformatresearch/2024/05/02/flac): Lossless audio sample format.
* 🆓📖 `.mka` [Matroska Audio](/fileformatresearch/2024/05/05/mka): Matroska audio. Used to encapsulate complex audio files or as components of other Matroska formats.

Read only:

* 🆓📖 `.mp3` [MP3](/fileformatresearch/2024/05/02/mp3): Lossy audio sample format.
* 🆓📖 `.wav` [Waveform Audio File Format](/fileformatresearch/2024/05/05/wav): An audio file format. It uses the linear pulse-code modulation (LPCM).

### Archive

#### Optical Disc Archive

* 🆓📖 `.iso` [ISO](/fileformatresearch/2024/04/11/iso): An optical disc file system image file format.

#### Universal File System Archive

* 🆓📖 `.7z` [7Z](/fileformatresearch/2024/04/10/7z): General archive and compression format with more function and better compression ratio than ZIP. But not many file formats use 7Z as the base format.

Read only:

* 💰📕 `.rar` [RAR](/fileformatresearch/2024/04/10/rar): Archive and compression format.
* 🆓📖 `.zip` [ZIP](/fileformatresearch/2024/04/10/zip): General archive and compression format, also as the basis for many other file formats.
* 🆓📖 `.bz2` [Bzip2](/fileformatresearch/2024/04/10/bzip2-format): Single file compression format.
* 🆓📖 `.gz` [Gzip](/fileformatresearch/2024/04/10/gzip): Single file compression format.
* 🆓📖 `.tar` [Tar](/fileformatresearch/2024/04/10/tar): Archive file format. One advantage of this format is that Tar can save file permission information on file systems of Unix-like systems. But I personally think it's better to include a shell script with the archive to set the file permissions. This eliminates the need to use a tar archive.
* 🆓📖 `.xz` [XZ](/fileformatresearch/2024/04/10/xz): Single file compression format.

### Bibliography Data

* 🆓📖 `.bib` [BibTeX](/fileformatresearch/2024/04/15/bib): A data format for recording citation sources.

### C Compiler Source Files

* 🆓📖 `.c` [C Programming Language Source File](/fileformatresearch/2024/05/05/c-source): Source code file format of the C programming language.
* 🆓📖 `.h` [C Programming Language Header File](/fileformatresearch/2024/05/05/c-header): Header file format of the C programming language.

### C++ Compiler Source Files

* 🆓📖 `.cpp` [C++ Programming Language Source File](/fileformatresearch/2024/05/05/cpp-source): Source code file format of the C++ programming language.
* 🆓📖 `.hpp` [C++ Programming Language Header File](/fileformatresearch/2024/05/05/cpp-header): Header file format of the C++ programming language.

### Document Typesetting Description

#### Common Document Typesetting Description

* 🆓📖 `.md` [Markdown](/fileformatresearch/2024/04/10/markdown-format): A simple markup format used to write documents without complex style or structure.
* 🆓📖 `.tex` [TeX](/fileformatresearch/2024/04/15/tex): Markup language format for TeX typesetting system.

#### Web Page Style Sheet

* 🆓📖 `.css` [Cascading Style Sheets](/fileformatresearch/2024/04/19/css): A markup language used to describe the styles of HTML elements.
* 🆓📖 `.scss` [SCSS](/fileformatresearch/2024/04/19/scss): A markup language that generates CSS. It's like an extension to SCSS.

Read only:

* 🆓📖 `.sass` [Sass](/fileformatresearch/2024/04/19/sass): A markup language that generates CSS.It uses indentation to indicate code levels.

#### Web Page Typesetting

* 🆓📖 `.html` [HyperText Markup Language](/fileformatresearch/2024/04/19/html): Markup language for Web typesetting.

### E-document

#### Electronic Display

* 🆓📖 `.epub` [EPUB](/fileformatresearch/2024/04/10/epub): E-book format based on web related technologies.

Read only:

* 🆓📕 `.chm` [Microsoft Compiled HTML Help](/fileformatresearch/2024/04/17/chm): Compiled HTML documents.

#### Imitating Paper

* 🆓📖 `.pdf` [Portable Document Format](/fileformatresearch/2024/04/09/png): Mainly used as document format for both scanned and rendered, sometimes used as vector image format.

Read only:

* 🆓📖 `.djvu` [DjVu](/fileformatresearch/2024/04/10/djvu): Document format or pixel image format for scanned documents.

### Editable Document Container

* 🆓📖 `.docx` [Office Open XML Document](/fileformatresearch/2024/04/24/docx): Editable document container for Microsoft Office Word etc.

Read only:

* 💰📖 `.doc` [Microsoft Office Word Binary File Format](/fileformatresearch/2024/04/24/doc): Editable document file format.
* 🆓📖 `.odf` [OpenDocument Formula](/fileformatresearch/2024/04/24/odf): A format to save math formula typesetting.
* 🆓📖 `.odt` [OpenDocument Text](/fileformatresearch/2024/04/24/odt): An editable document file container format.

### Pixel Image

* 🆓📖 `.apng` [Animated PNG](/fileformatresearch/2024/04/09/apng): Lossless animated pixel image format.
* 🆓📖 `.jpg` [JPEG Format](/fileformatresearch/2024/04/09/jpeg): Lossy pixel image format.
* 🆓📖 `.png` [Portable Network Graphics](/fileformatresearch/2024/04/09/pdf): Lossless pixel image format.

Read only:

* 🆓📖 `.gif` [Graphics Interchange Format](/fileformatresearch/2024/04/09/gif): Lossless animated pixel image format.

### Plain Text

Files without extensions will be treated as plain text files by default. But there is still a suffix for plain text files:

* 🆓📖 `.txt` [Plain Text File](/fileformatresearch/2024/04/07/text-file): Basic text file format.

### PowerShell Runtime Environment

* 🆓📖 `.ps1` [PowerShell](/fileformatresearch/2024/04/19/pwsh-format): PowerShell script file.
* 🆓📖 `.psm1` [PowerShell Module](/fileformatresearch/2024/04/20/pwsh-module): PowerShell module file.
* 🆓📖 `.psd1` [PowerShell Manifest](/fileformatresearch/2024/04/20/pwsh-manifest): Manifest for generate PowerShell Module.

### Python Runtime Environment

* 🆓📖 `.py` [Python](/fileformatresearch/2024/04/19/python-source): A general programming language.

### Rust Compiler Source Files

* 🆓📖 `.rs` [Rust Programming Language Source File](/fileformatresearch/2024/05/05/rust-source): Source code file format of the Rust programming language.

### Timed Text

* 🆓📖 `.lrc` [LRC](/fileformatresearch/2024/05/05/lrc): A simple lyric file format. Mainly for music.
* 🆓📖 `.mks` [Matroska Subtitle](/fileformatresearch/2024/05/05/mks): Matroska subtitle. Used to encapsulate complex subtitle files or as components of other Matroska formats.
* 🆓📖 `.srt` [SubRip](/fileformatresearch/2024/05/05/srt): A plain text-based external subtitle format.

### Tabular Data

* 🆓📖 `.xlsx` [Office Open XML Workbook](/fileformatresearch/2024/04/28/xlsx): Spreadsheet file format, used for display tables or simple data tables, with some data processing functions.

Read only:

* 💰📖 `.xls` [Microsoft Office Excel Binary File Format](/fileformatresearch/2024/04/28/xls): A data sheet file format.
* 🆓📖 `.ods` [OpenDocument Spreadsheet](/fileformatresearch/2024/04/28/ods): A spreadsheet file format.
* 🆓📖 `.csv` [Comma-Separated values](/fileformatresearch/2024/04/21/csv): A simple markup language for representing tabular data. Use comma as delimiters. There are some variations of it. They are collectively called "Delimiter-seperated". Delimiter-seperated values are not as good as binary files in terms of compression rate, and are not as good as XML, JSON, etc. in terms of scalability and data type richness.
* 🆓📖 `.tsv` [Tab-Separated Values](/fileformatresearch/2024/04/21/tsv): A simple markup language for representing tabular data. Use horizontal tabs as delimiters.

### Universal Markup Data

Although these file formats can theoretically replace each other, their different syntax designs cause them to have different adaptability to different scenarios. Generally, one or more of them are selected according to the needs or framework requirements. So there are multiple alternatives juxtaposed.

* 🆓📖 `.json` [JavaScript Object Notation](/fileformatresearch/2024/04/21/json): A lightweight data markup language.
* 🆓📖 `.toml` [Tom's Obvious Minimal Language](/fileformatresearch/2024/04/21/toml): A simple config file format.
* 🆓📖 `.xml` [Extensible Markup Language](/fileformatresearch/2024/04/09/xml): A common data representation format.
* 🆓📖 `.yml` [YAML](/fileformatresearch/2024/04/19/yaml): An easy-to-read data file format.

### Unix-like System Shell Script

A type of shell script mainly used on Unix systems (mainly for: Bourne Shell, Bash etc.). Overall the syntax is archaic and strange. Sometimes adding an extra space before or after an operator can cause errors.

* 🆓📖 `.sh` [Bourne Shell](/fileformatresearch/2024/04/19/sh-format): Universal system management script for Unix.
* 🆓📖 `.profile` [Bourne Shell Config](/fileformatresearch/2024/04/19/sh-config): The file used for the initial configuration of the Bourne Shell. It is also supported by many other shells.
* 🆓📖 `.bashrc` [Bash Config](/fileformatresearch/2024/04/19/bash-config): Script for setting up Bash.

### Vector Font

* 🆓📖 `.otc` [PostScript-flavored OpenType Collection](/fileformatresearch/2024/04/14/opentype-collection): Vector font collection file format. Mainly used for GUI operating systems.
* 🆓📖 `.otf` [PostScript-flavored OpenType](/fileformatresearch/2024/04/14/opentype): Vector font file format. Mainly used for GUI operating systems.
* 🆓📖 `.woff2` [WOFF2](/fileformatresearch/2024/04/14/woff2): Vector font file for web.

Read only:

* 🆓📖 `.ttc` [TrueType-flavored OpenType Collection](/fileformatresearch/2024/04/14/truetype-collection): Vector font collection file format.
* 🆓📖 `.ttf` [TrueType-flavored OpenType](/fileformatresearch/2024/04/14/truetype): Vector font file format.
* 🆓📖 `.woff` [WOFF](/fileformatresearch/2024/04/14/woff): Vector font file for web.

### Vector Image

#### Chart Drawing

* 💰📕 `.vsdx` [Visio XML Format](/fileformatresearch/2024/04/28/vsdx): A diagram file format based on XML and ZIP.

Read only:

* 💰📕 `.vsd` [Microsoft Office Visio Binary File Format](/fileformatresearch/2024/04/28/vsd): A diagram file format.
* 🆓📖 `.odg` [OpenDocument Graphics](/fileformatresearch/2024/04/28/odg): A vector image and diagram file format.

#### Common Vector Image Format

* 🆓📖 `.svg` [Scalable Vector Graphics](/fileformatresearch/2024/04/09/svg): Vector image format.

#### Interactive vector animation

* 🆓📖 `.pptx` [Office Open XML Presentation](/fileformatresearch/2024/04/28/pptx): An interactive graphic file format.

Read only:

* 💰📖 `.ppt` [Microsoft Office PowerPoint Binary File Format](/fileformatresearch/2024/04/28/ppt): An interactive graphic file.
* 🆓📖 `.odp` [OpenDocument Presentation](/fileformatresearch/2024/04/28/odp): An interactive graphic file format.

### Video Container

* 🆓📖 `.mkv` [Matroska Video](/fileformatresearch/2024/05/05/mkv): Matroska video. Used to encapsulate complex audiovisual files.
* 🆓📖 `.mp4` [MP4](/fileformatresearch/2024/05/05/mp4): A common audio and video container formats. Used to encapsulate relatively simple audio and video streams.

Read only:

* 🆓📖 `.avi` [Audio Video Interleave](/fileformatresearch/2024/05/05/avi): An audio and video file format dominated by Microsoft.
* 🆓📖 `.flv` [Flash Video](/fileformatresearch/2024/05/05/flv): An audio and video container for Adobe Flash.
