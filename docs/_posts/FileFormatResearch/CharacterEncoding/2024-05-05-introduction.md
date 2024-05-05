---
title: "Character Encoding and Plain Text File Format"
date: 2024-05-05 22:15:03 +0800
category: CharacterEncodingResearch
tags:
header:
  teaser: https://upload.wikimedia.org/wikipedia/commons/8/8e/Roadmap_to_Unicode_BMP.svg
---

Character encoding schemes map characters to binary data. They are fundamental in both file formats and programming data representation.

## Character Encoding Schemes

ZhiZe recommends using Unicode's UTF family encoding scheme:

* Unicode

The following are some of the schemes that are Unicode compatible or related:

* ASCII
* ISO 8859

The following encoding schemes can be replaced by Unicode or are deprecated:

* Big5
* GB Character Encoding Scheme Series
* IBM PC Code Page 437
* JIS Character Encoding Scheme Series
* KS X Character Encoding Scheme Series

## File Format

Files without extensions will be treated as plain text files by default. If you want to add a suffix to a plain text file, use the following suffix:

* 🆓📖 `.txt` [Plain Text File](/fileformatresearch/2024/04/07/text-file): Basic text file format.

Plain text files use UTF-8 encoding by default. Other UTF series encodings will add a BOM (Byte Order Mark) at the beginning of the file by default. They can therefore be distinguished from UTF-8.

## Character or String Representation in Programming Models

Different programming languages use different encoding schemes. Which variant of UTF a programming language uses by default is determined by the programming language specification.

Generally speaking, even if a programming language uses UTF-16 or UTF-32 as the default character and string encoding scheme, it will not add a BOM at the beginning of the character or string data structure explicitly. Byte order is determined by the programming language's compiler or runtime environment.
