---
date: 2019-10-11
keywords: "toml,.toml,toml 文件格式,如何打开 toml 文件,.toml 扩展名,toml 扩展名"
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "TOML 文件格式"
linktitle: "TOML"
description: "了解 TOML 文件格式和可以创建和打开 TOML 文件的 API。"
menu:
  docs:
    parent: "programming"
lastmod: 2020-12-01
---

## 什么是一 .toml 文件？ ##

TOML（Tom's Obvious Minimal Language）是一种使用 .toml 扩展名的最小配置文件格式。 TOML 旨在易于阅读，明确映射到字典，并易于解析为不同的数据结构。 TOML 有一个收到社区贡献的开源规范。许多编程语言都支持 TOML，例如 C、C#、Dart、Elixir、Erlang、Go、Java、PHP、Python、Ruby、Swift 等。TOML 文件的 MIME 类型是 *application/toml*。


## TOML 文件格式##

TOML 文件主要由键/值对、节/表、注释组成，并且必须是有效的 UTF-8 编码的 Unicode 文档。 TOML 支持 String、Integer、Float、Boolean、Datetime、Array 和 Table(hash table/dictionary) 数据类型。 TOML 是一种区分大小写的语言。

＃＃＃ 句法 ＃＃＃

- **键值对**：键值对由等号 (=) 分隔。每对必须在一个新行上。

```汤姆
第一个=“汤姆"
最后=“普雷斯顿-维尔纳"
```

- **评论**：评论以井号 (#) 符号开头。

```汤姆
# 这是一个 TOML 文档。
```

- **字符串**：字符串用引号 (") 括起来。

```汤姆
string = "示例字符串"
```

- **多行字符串**：多行字符串用三个引号 (""") 括起来。

```汤姆
[家庭地址]
street = """123 龙卷风巷
套房 16"""
city = "东森特维尔"
状态 = "KS"
```

- **整数/浮点数**

```汤姆
整数 = 20
浮动 = 20.5
```

- **布尔值**：布尔值始终为小写。

```汤姆
bool1 = 真
bool2 = 假
```

- **日期时间**：对于日期时间，您可以使用 RFC 3339 格式的日期时间，如下例所示。

```汤姆
offset_date_time = 1979-05-27 07:32:00Z
local_date_time = 1979-05-27T07:32:00
本地日期 = 1979-05-27
local_time = 07:32:00
```

- **数组**：数组用方括号括起来，元素之间用逗号 (,) 分隔。

```汤姆
颜色 = [“红色"、“黄色"、“绿色"]
```

- **表**：表是键/值对的集合，由方括号 ([]) 包围的新行上的标题定义。当提供新标题或文件结束时，表格结束。

```汤姆
[家庭地址]
street = """123 龙卷风巷
套房 16"""
city = "东森特维尔"
状态 = "KS"

[办公地址]
street = """123 龙卷风巷
套房 16"""
city = "东森特维尔"
状态 = "KS"
```

内联表由花括号 ({}) 包围，每个键/值对由逗号 (,) 分隔。

```汤姆
姓名 = { 第一 = “汤姆"，最后 = “皮特" }
```

## 参考 ＃＃

- [TOML - 维基百科](https://en.wikipedia.org/wiki/TOML)
- [TOML](https://toml.io/en/)

