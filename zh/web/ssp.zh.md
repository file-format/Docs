---
date: 2021-07-05
keywords: "ssp,.ssp,ssp 文件格式,如何打开 ssp 文件,Scala 服务器页面"
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: "SSP - Scala 服务器页面文件格式"
linktitle: "SSP"
description: "了解什么是 SSP 文件格式以及可以创建和打开 SSP 文件的 API。"
menu:
  docs:
    identifier: "web-ssp"
    parent: "web"
lastmod: 2021-09-30
---

## 什么是一 .ssp 文件？

扩展名为 .ssp 的文件是使用 Scala 代码创建的网页，用于表达式，而不仅仅是纯 HTML。它使用 HTML 和 Scala 的组合充当服务器端脚本。这些文件驻留在服务器上，用于创建提供给用户的静态网页。 Scala 本身是一种通用编程语言，其语法对于使用过 Velocity、JSP 或 Erb 的用户来说是熟悉的。 SSP 文件可以使用 [Scalate](https://scalate.github.io/scalate/) 进行分析和评估，这是一个基于 Scala 的模板引擎，用于生成文本和标记。

## SSP 文件格式 - 更多信息

SSP 文件保存在纯文本文件中，可以使用 Scalate 进行评估。 Ssp 模板由纯文本组成，通常是 HTML 文档。它嵌入了 Ssp 标签，使渲染引擎动态地渲染文档的不同部分。标签以 <% ... %> 和 ${ ... } 序列开头和结尾，并且这些之外的任何内容都被视为文字文本。

### SSP 示例

以下示例显示了 SSP 代码及其在渲染引擎渲染时的输出。

```PHP
<p>
  <%= List("hi", "there", "reader!").mkString(" ") %>
  ${ "yo "+(3+4) }
</p>
```
输出如下。
```
<p>
  hi there reader!
  yo 7
</p>
```

## 参考

- [SSP 参考](https://scalate.github.io/scalate/documentation/ssp-reference.html)

