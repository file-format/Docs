---
date: 2019-10-11
keywords: "json, .json, json 文件格式, 如何打开 json 文件, javascript 对象表示法, json 数据格式, .json 文件格式"
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "JSON 文件格式 - 什么是 JSON 文件？"
linktitle: "JSON"
description: "了解 JSON 文件格式和可以创建和打开 JSON 文件的 API。"
menu:
  docs:
    parent: "web"
lastmod: 2020-04-12
---

## 什么是 JSON 文件？

JSON（JavaScript 对象表示法）是一种用于共享数据的开放标准文件格式，它使用人类可读的文本来存储和传输数据。 JSON 文件以 .json 扩展名存储。 JSON 需要较少的格式，是 [XML](/zh/web/xml/) 的一个很好的替代方案。 JSON 源自 JavaScript，但它是一种独立于语言的数据格式。许多现代编程语言都支持 JSON 的生成和解析。 *application/json* 是用于 JSON 的媒体类型。

## JSON 文件格式 - 简史

需要导致创建 JSON 的实时服务器到客户端通信。 JSON 格式由 Douglas Crockford 于 2001 年 3 月首次指定。JSON 基于标准 ECMA-262 第 3 版 — 1999 年 12 月，它是 JavaScript 的子集。

JSON 标准 ECMA-404 的第一版于 2013 年 10 月由 Ecma International 发布。 RFC 7159 在 2014 年成为 JSON 互联网使用的主要参考。2017 年 11 月，ISO/IEC 21778:2017 作为国际标准发布。 RFC 8259 于 2017 年 12 月 13 日由 Internet 工程任务组发布，它是 Internet 标准 STD 90 的当前版本。

## JSON 文件结构

JSON 数据以 **key/value** 对形式写入。键和值由中间的冒号(:) 分隔，键在左边，值在右边。不同的键/值对由逗号 (,) 分隔。键是一个用双引号括起来的字符串，例如“name"。这些值可以是以下类型。

- `数字`
- `String`：由双引号括起来的 Unicode 字符序列。
- `布尔`：真或假。
- `Array`：用方括号括起来的值列表，例如

```json
[“苹果"、“香蕉"、“橙子"]
```

- `Object`：由花括号包围的键/值对的集合，例如

```json
{"name": "Jack", "age": 30, "favoriteSport": "Football"}
```

JSON 对象也可以嵌套来表示数据的结构。下面给出的是 JSON 对象的示例。

### JSON 格式示例

```json
{
   "name":"Jack",
   "age":30,
   "contactNumbers":[
      {
         "type":"Home",
         "number":"123 123-123"
      },
      {
         "type":"Office",
         "number":"321 321-321"
      }
   ],
   "spouse":null,
   "favoriteSports":[
      "Football",
      "Cricket"
   ]
}
```

## JSON 文件的最大大小是多少？

JSON 文件的最大大小实际上没有限制。它可以与要存储的内容所需的空间一样长。

在使用 JSON 文件格式通过 Internet 传输数据时，需要注意计算机的可用资源。如果传输较大的 JSON 数据，如果客户端浏览器内存有限，传输将受到影响。


规范没有定义硬性限制，但是您需要注意不要耗尽用户计算机上的资源，因为这会很快降低他们的用户体验，并且他们很可能会放弃您的应用程序。

## JSON 与 XML

**XML** 是另一种常见且广泛使用的文件格式，用于通过 Internet 交换数据。在应用程序之间交换数据时，开发人员可以选择使用 XML 和 JSON 文件格式。然而，由于以下原因，JSON 被采用作为应用程序之间通过 Internet 进行数据交换的最便捷方式。

1. 与 XML 文件格式相比，JSON 提供了清晰易读的数据视图
1. JSON 减少了通过 Internet 传输数据的开销，因为与 XML 相比，它具有更少的字符来定义相同的数据集
1. 现代编程语言提供内置解析器来解析 Web 上的 JSON 响应。

## 你可知道？

您可以成为 FileFormat.com 的贡献者，让文件格式社区及时了解您的发现。如果您必须分享有关 JSON 或 Web 文件格式的任何内容，您可以在 [Web File Format News](https://news.fileformat.com/t/Web) 部分发布您的发现，以便人们从这些中了解更多信息。

## 参考

- [JSON - 维基百科](https://en.wikipedia.org/wiki/CSS)
- [JSON 简介](https://www.digitalocean.com/community/tutorials/an-introduction-to-json)

