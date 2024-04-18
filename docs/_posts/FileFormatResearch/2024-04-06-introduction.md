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

## Recommendations

### Common Use

#### Archive and Compression

* 🆓📖 [7Z](/fileformatresearch/2024/04/10/7z): General archive and compression format with more function and better compression ratio than ZIP. But not many file formats use 7Z as the base format.
* 🆓📖 [ISO](/fileformatresearch/2024/04/11/iso): An optical disc file system image file format.
* 🆓📖 [ZIP](/fileformatresearch/2024/04/10/zip): General archive and compression format, also as the basis for many other file formats.

Read only:

* 💰📕 [RAR](/fileformatresearch/2024/04/10/rar): Archive and compression format.

#### Bibliography Data

* 🆓📖 [BibTeX](/fileformatresearch/2024/04/15/bib): A data format for recording citation sources.

#### Document Release

* 🆓📖 [EPUB](/fileformatresearch/2024/04/10/epub): E-book format based on web related technologies.
* 🆓📖 [Portable Document Format](/fileformatresearch/2024/04/09/png): Mainly used as document format for both scanned and rendered, sometimes used as vector image format.

Read only:

* 🆓📖 [DjVu](/fileformatresearch/2024/04/10/djvu): Document format or pixel image format for scanned documents.
* 🆓📕 [Microsoft Compiled HTML Help](/fileformatresearch/2024/04/17/chm): Compiled HTML documents.

#### Font

* 🆓📖 [PostScript-flavored OpenType](/fileformatresearch/2024/04/14/opentype): Vector font file format. Mainly used for GUI operating systems.
* 🆓📖 [PostScript-flavored OpenType Collection](/fileformatresearch/2024/04/14/opentype-collection): Vector font collection file format. Mainly used for GUI operating systems.
* 🆓📖 [WOFF2](/fileformatresearch/2024/04/14/woff2): Vector font file for web.

Read only:

* 🆓📖 [WOFF](/fileformatresearch/2024/04/14/woff): Vector font file for web.

#### Markup Document

* 🆓📖 [Markdown](/fileformatresearch/2024/04/10/markdown-format): A simple markup format used to write documents without complex style or structure.

#### Plain Text Data

* 🆓📖 [Extensible Markup Language](/fileformatresearch/2024/04/09/xml): A common data representation format.
* 🆓📖 [Plain Text File](/fileformatresearch/2024/04/07/text-file): Basic text file format.

#### Typesetting

* 🆓📖 [TeX](/fileformatresearch/2024/04/15/tex): Markup language format for TeX typesetting system.

#### Vector Image

* 🆓📖 [Scalable Vector Graphics](/fileformatresearch/2024/04/09/svg): Vector image format.

### Human Perceptual Media

#### Audio Sampling

#### Pixel Image

* 🆓📖 [Animated PNG](/fileformatresearch/2024/04/09/apng): Lossless animated pixel image format.
* 🆓📖 [Portable Network Graphics](/fileformatresearch/2024/04/09/pdf): Lossless pixel image format.
* 🆓📖 [JPEG Format](/fileformatresearch/2024/04/09/jpeg): Lossy pixel image format.

Read only:

* 🆓📖 [Graphics Interchange Format](/fileformatresearch/2024/04/09/gif): Lossless animated pixel image format.

#### Video Containers

### System Compatible

#### Unix-like System Archive and Compression

On Unix-like systems, archiving and compression are treated as two operations. Tar is responsible for archiving, and other softwares is responsible for compressing. This is a relatively complex process to use.

One advantage of these software is that Tar can save file permission information on file systems of Unix-like systems. But I personally think it's better to include a shell script with the archive to set the file permissions. This eliminates the need to use a tar archive.

* 🆓📖 [Bzip2](/fileformatresearch/2024/04/10/bzip2): Single file compression format.
* 🆓📖 [Gzip](/fileformatresearch/2024/04/10/gzip): Single file compression format.
* 🆓📖 [Tar](/fileformatresearch/2024/04/10/tar): Archive file format.
* 🆓📖 [XZ](/fileformatresearch/2024/04/10/xz): Single file compression format.

#### TrueType Compatible System Font

These are mainly used for systems that don't have good support for `.otf`. Such systems should be gradually reduced in the future. At that time, TrueType-flavored fonts will also use the `.otf` suffix.

* 🆓📖 [TrueType-flavored OpenType](/fileformatresearch/2024/04/14/truetype): Vector font file format.
* 🆓📖 [TrueType-flavored OpenType Collection](/fileformatresearch/2024/04/14/truetype-collection): Vector font collection file format.

## Trend

Trends in file format recommendation changes.
