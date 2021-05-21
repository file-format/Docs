---
date: 2019-10-11
keywords: toml, .toml, toml file format, how to open toml files, .toml extension, toml extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: TOML File Format
linktitle: TOML
description: Learn about TOML file format and APIs that can create and open TOML files.
menu:
  docs:
    parent: "programming"
lastmod: 2020-12-01
---

## What is a TOML file? ##

TOML (Tom's Obvious Minimal Language) is a minimal configuration file format that uses the .toml extension. TOML aims to be easy to read, to map unambiguously to dictionaries, and to be easy to parse to different data structures. TOML has an open-source specification that received community contributions. TOML is supported by many programming languages like C, C#, Dart, Elixir, Erlang, Go, Java, PHP, Python, Ruby, Swift, etc. The MIME type for TOML files is *application/toml*.


## TOML File Format ##

TOML files mainly consist of key/value Pairs, sections/tables, comments and must be a valid UTF-8 encoded Unicode document. TOML supports String, Integer, Float, Boolean, Datetime, Array, and Table(hash table/dictionary) data types. TOML is a case-sensitive language.

### Syntax ###

- **Key-Value Pairs**: Key-value pairs are separated by equals sign (=). Each pair must be on a new line.

  ```toml
  first = "Tom"
  last = "Preston-Werner"
  ```

- **Comments**: Comments begin with the hash (#) symbol.

  ```toml
  # This is a TOML document.
  ```

- **Strings**: Strings are surrounded by quotation (") marks.

  ```toml
  string = "Example String"
  ```

- **Multi-line Strings**: Multi-line Strings are surrounded by three quotation (""") marks.

  ```toml
  [home address]
  street = """123 Tornado Alley 
  Suite 16"""
  city = "East Centerville"
  state = "KS"
  ```

- **Integers/Floats**

  ```toml
  integer = 20
  float = 20.5
  ```

- **Booleans**: Booleans are always lowercase.

  ```toml
  bool1 = true
  bool2 = false
  ```

- **Date-Time**: For DateTime, you may use an RFC 3339 formatted date-time as shown in the example below.

  ```toml
  offset_date_time = 1979-05-27 07:32:00Z
  local_date_time = 1979-05-27T07:32:00
  local_date = 1979-05-27
  local_time = 07:32:00
  ```

- **Arrays**: Arrays are surrounded by square brackets with elements separated by commas (,).

  ```toml
  colors = [ "red", "yellow", "green" ]
  ```

- **Tables**: Tables are collections of key/value pairs that are defined by headers on a new line surrounded by square brackets ([]). The table ends when a new header is provided or when the file ends.

  ```toml
  [home address]
  street = """123 Tornado Alley 
  Suite 16"""
  city = "East Centerville"
  state = "KS"

  [office address]
  street = """123 Tornado Alley 
  Suite 16"""
  city = "East Centerville"
  state = "KS"
  ```

  Inline tables are surrounded by curly braces ({}) with each key/value pair separated by comma (,).

  ```toml
  name = { first = "Tom", last = "Pitt" }
  ```

## References ##

- [TOML - Wikipedia](https://en.wikipedia.org/wiki/TOML)
- [TOML](https://toml.io/en/)
