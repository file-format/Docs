---
date: 2019-10-11
keywords: "step, .step, step 文件格式, 如何打开 step 文件, .step 扩展名, step 扩展名"
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "步骤文件格式"
linktitle: "步"
description: "了解可以创建和打开 STEP 文件的 STEP 文件格式和 API。"
menu:
  docs:
    parent: "3d"
lastmod: 2020-18-01
---

## 什么是 .STEP 文件？

STEP 文件是一种广泛使用的计算机辅助设计 (CAD) 数据交换格式。它于 1994 年由 ISO 委员会以“ISO 10303-21"的名义标准化。 ISO 10303-21 定义了以 EXPRESS 数据建模语言表示数据的编码机制。 STEP 文件也称为 p21 文件和 STEP 物理文件。用于 STEP 文件的文件扩展名为 .stp 和 .step。

## 基本历史

1994 年，最初的 Part 21 规范发布。它有一些错误，已在 1996 年发布的技术更正中得到纠正。第二版于 2002 年发布，其中包括更正和几个数据部分的扩展。第三版于 2016 年发布，增加了锚点和参考部分，允许将实体和值存储在外部文件中。添加了对字符串的 UTF-8 支持。添加了数字签名以验证文件的内容并验证凭据。还添加了对使用 ZIP 压缩和存储交换结构的支持。

## 步骤文件格式

STEP 文件的纯文本格式由一系列记录组成。字符集定义为 ISO 10646 的代码点。“ISO-10303-21;"是第一条记录中的第一个字符。注释被“/*"和“*/"字符包围。最后一条记录包含“END-ISO-10303-21;"如果 STEP 文件符合 2002 版本。如果符合2016版，“END-ISO-10303-21"后面可能有一个或多个数字签名；终结者。换行符用“\N\"表示，分页符用“\F\"表示。

STEP 文件分为多个部分，它们的名称是保留术语。所有部分都以“ENDSEC"记录结尾，并且必须按照下面显示的顺序。

- **HEADER**：这是强制性且不可重复的部分。它由以下实体组成：
  - file_description (mandatory)
  - file_name (mandatory)
  - file_schema (mandatory)
  - schema_population (optional)
  - file_population (optional)
  - section_language (optional)
  - section_context (optional)
- **ANCHOR**：这是一个可选的非重复部分，在 2016 版本中引入。它定义了实例的外部名称，以便可以引用它们。
- **参考**：这是一个可选的非重复部分，也在 2016 版中引入。本节中的每个条目都将条目/值实例名称与外部文件中的实例/值相关联。
- **DATA**：这是一个可选的可重复部分，包含模型实例的核心内容。
- **SIGNATURE**：这是 2016 版中引入的可选可重复部分。它持有数字签名以验证文件的内容或验证凭据。

## 参考

- [ISO 10303-21 - 维基百科](https://en.wikipedia.org/wiki/ISO_10303-21)

