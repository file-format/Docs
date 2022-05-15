---
date: 2022-05-09
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: PYM File Format - PYM Macro Preprocessor File
linktitle: PYM
description: Learn about PYM file format and APIs that can create and open PYM files.
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## What is a PYM file?

A PYM file is a macro preprocessor file based on the Python programming language. It was developed by VRVis Research and store macro shortcuts. When the PYM file is interpreted by the Python interpreter's preprocessing stage, these shortcuts are expanded as replacements for their full text. In addition, a third, optional operation that can be performed by a macro preprocessor is file inclusion. PYM files can be opened in text editors such Notepad, Notepad++, Apple TextEdit, and VI on Linux.

## PYM File Format

PYM files are saved as plain text files to disc. A PYM file can also include other files using the `#include` directive.

### PYM Syntax

PYM statements are included between ""#begin python and "#end python" markers as shown below.

```
we decided to use a line based special sequence to introduce PYM macros:

#begin python

#python code for defining "macros" goes here

#end python
```
### PYM Macro Expansion

The PYM macro expansion is represented by two sequences i.e. <[ and ]>. These are special html tags and can appear anywhere in a line. A little PYM example is as follow.

```
#begin python
TITLE = "My Web page"
def EXP(e): return str(e)
#end python
<head>
<title><[TITLE]></title>
</head>
<body>
<h4><[TITLE]></h4>
<p>The value of 2 raised to the 4th power is <[EXP(2**4)]>.</p>
</body>
```

The output of running this through PYM is as follow:

```
<head>
<title>My Web Page</title>
</head>
<body>
<h4>My Web Page</h4>
<p>The value of 2 raised to the 4th power is 16.</p>
</body>
```

## References ##

 * [PYM - A Macro Preprocessor Based on Python](http://web.archive.org/web/20051122185426/http://ray.cg.tuwien.ac.at/rft/Papers/PYM/pym.html)
 * [PYM Interpreters](https://github.com/interpreters/pym)
