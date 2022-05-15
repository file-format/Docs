---
date: 2022-05-09
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: PYI File Format - Python Interface Definition
linktitle: PYI
description: Learn about PYI file format and APIs that can create and open PYI files.
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## What is a PYI file?

A PYI file is a Python Interface Definition file that contains code stub reference for implementation of the interface. Each Python module is represented as a .pyi stub which is a normal Python file but with empty methods. The syntax of PYI files is the same as that of a regular Python module. The implementation of the empty methods is left for end-user to achieve specific objective for which the module is written. That is where PYI files are different than [PY](/programming/py/) files which contain complete implementation of the program. PYI files can be opened with text editors such as Notepad, Notepad++, Microsoft Visual Studio Code, and JetBrains PyCharm.

## PYI File Format

PYI files are saved as plain text files that can be opened with any text editor. Python is an interpreter language that performs type checking when the code is executed. In such case, PYI files are beneficial in the way that developers can manually define and check a module's types while writing the application.

## References ##

 * [Interfaces - Java](https://en.wikipedia.org/wiki/Interface_(Java))
 * [PYM Interpreters](https://github.com/interpreters/pym)
