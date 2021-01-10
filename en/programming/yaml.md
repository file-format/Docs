---
date: 2019-10-11
keywords: yaml, .yaml, yaml file format, how to open yaml files, .yaml extension, yaml extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: YAML File Format
linktitle: YAML
description: Learn about YAML file format and APIs that can create and open YAML files.
menu:
  docs:
    parent: "programming"
lastmod: 2020-25-11
---

## What is a YAML file? ##

YAML (YAML Ain't Markup Language) is a Unicode based data-serialization language that is used for configuration files, internet messaging, object persistence, etc. YAML uses the .yaml extension for its files. YAML was designed to work well with modern programming languages.

## Brief History ##

YAML was first proposed in 2001 and was developed by Clark Evans, Ingy döt Net, and Oren Ben-Kiki. YAML was first said to mean "Yet Another Markup Language" to indicate its purpose as a markup language. It was later repurposed as "YAML Aint Markup Language" to indicate its purpose as data-oriented.

## How to open YAML files ##

To open YAML files, you can use the following:

- Notepad
- Notepad++
- VS Code
- Atom
- IntelliJ IDEA

## YAML File Format ##

YAML file consists of the following data types

- **Scalars**: Scalars are values like Strings, Integers, Booleans, etc.
- **Sequences**: Sequences are lists with each item starting with a hyphen (-). Lists can also be nested.
- **Mappings**: Mapping gives the ability to list keys with values.

## Syntax ##

- **Whitespace**: Whitespace indentation is used to indicate nesting and overall structure.

  ```yaml
  name: John Smith
  contact:
      home:   1012355532
      office:  5002586256
  address:
    street: |
              123 Tornado Alley
              Suite 16
      city:   East Centerville
      state:  KS
  ```

- **Comments**: Comments are written beginning with the "#" symbol.

  ```yaml
  # This is a YAML Comment
  ```

- **Lists**: Hyphen (-) is used to indicate list members with each member on a separate line. List members can also be enclosed in square brackets ([...]) with members separated by commas (,).

  ```yaml
  - A
  - B
  - C
  ```

  ```yaml
  [A, B, C]
  ```

- **Associative Array**: An associative array is surrounded by curly brackets ({...}). The keys and values are separated by colon(:) and each pair is separated by comma (,).

  ```yaml
  {name: John Smith, age: 20}
  ```

- **Strings**: String can be written with or without double-quotes (") or single-quotes (').

  ```yaml
  Sample String
  "Sample String"
  'Sample String'
  ```

- **Scalar Block content**: Scalar content can be written in block notation by using the following:
  - **|**: All live breaks are significant.
  - **>**: Each line break is folded to space. It removes the leading whitespace for each line.

  ```yaml
  data: |
    YAML 
      (YAML Ain't Markup Language)
    is a data-serialization language
  ```

  ```yaml
  data: ?
    YAML (YAML Ain't Markup Language)
    is a data-serialization language
  ```

- **Multiple Documents**: Multiple documents are separated by three hyphens (---) in a single stream. Hyphens indicate the start of the document. Hyphens are also used to separate directives from document content. The end of the document is indicated by three dots (...).

  ```yaml
  ---
  Document 1
  ---
  Document 2
  ...
  ```

- **Type**: To specify the type of value, double exclamation marks (!!) are used.

  ```yaml
  a: !!float 123
  b: !!str 123
  ```

- **Tag**: To assign a tag to a note, an ampersand (&) is used and to reference that node, an asterisk (*) is used.

  ```yaml
  name: John Smith
  bill-to:  &id01
    street: |
            123 Tornado Alley
            Suite 16
    city:   East Centerville
    state:  KS

  ship-to:  *id01
  ```

- **Directives**: YAML documents can be preceded by directives in a stream. Directives begin with a percent sign (%) followed by the name and then the parameters separated by spaces.

  ```yaml
  %YAML 1.2
  ---
  Document content
  ```

## References ##

- [YAML - Wikipedia](https://en.wikipedia.org/wiki/YAML)
- [YAML](https://yaml.org/spec/1.2/spec.html)
