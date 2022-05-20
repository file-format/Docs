---
date: 2021-07-05
keywords: ssp, .ssp, ssp file format, how to open ssp files, Scala Server Page
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SSP - Scala Server Pages
linktitle: SSP
description: Learn about what is an SSP file format and APIs that can create and open SSP files.
menu:
  docs:
    identifier: "web-ssp"
    parent: "web"
lastmod: 2021-09-30
---

## What is a SSP file?

A file with .ssp extension is web page created with Scala code for expressions instead of plain HTML only. It acts as a server side script using the combination of HTML and Scala. These files reside on the server and are used to create static webpages to be served to users. Scala itself is a general-purpose programming language whose syntax is familiar to users who have worked with Velocity, JSP or Erb. SSP files can be analyzed and evaluated using [Scalate](https://scalate.github.io/scalate/) which is a Scala based template engine for generating text and markup.

## SSP File Format - More Information

SSP files are saved in plain text file and can be evaluated using Scalate. An Ssp template consists of plain text which is more often the HTML document. It has Ssp tags embedded in it that causes the rendering engines to render different portions of the document dynamically. The tags start and end with <% ... %> and ${ ... } sequence and anything outside these is considered as literal text.

### SSP Example

The following example shows SSP code and its output when it is rendered by the rendering engine.

```PHP
<p>
  <%= List("hi", "there", "reader!").mkString(" ") %>
  ${ "yo "+(3+4) }
</p>
```
The output is as following.
```
<p>
  hi there reader!
  yo 7
</p>
```

## References

- [SSP Reference](https://scalate.github.io/scalate/documentation/ssp-reference.html)
