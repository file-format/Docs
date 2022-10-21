---
date: 2020-11-11
keywords: "myi, .myi, myi 文件格式, 如何打开 myi 文件, .myi 扩展名, myi 扩展名"
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "MYI 文件格式"
linktitle: "我的我"
description: "了解 MYI 文件格式和可以创建和打开 MYI 文件的 API。"
menu:
  docs:
    parent: "database"
lastmod: 2020-13-01
---

## 什么是 MYI 文件？ ##

MYI 也称为 MySQL MyISAM 索引文件。它用于存储 MySQL 的 MyISAM 表的索引。 MySQL 数据库索引定义了表的结构并包含检查表完整性的控制机制。

## MYI 文件格式##

MYI 文件有两部分，标题和键值。

### MYI 标题 ###

标头包含有关选项、文件大小和键的信息。 MySQL 中的键是使用类似的命令创建的

```sql
CREATE [UNIQUE] INDEX.
```

读取和写入 MYI 文件的文件位于 ./myisam 目录中。它有以下文件：

- mi_open.c：此文件包含编写标题每个部分的例程。
- mi_create.c：此文件包含调用 mi_open.c 例程的例程。
- myisamdef.h：这个文件有结构定义。

标题包含以下部分：

- state：状态由 mi_open.c、mi_state_info_write() 写入。此结构在文件中出现一次。
- 基础：基础由 mi_open.c、mi_base_info_write() 编写。 MI_BASE_INFO 是 myisamdef.h 中 base 的相应结构。此结构在文件中出现一次。
- keydef：keydef 由 mi_open.c、mi_keydef_write() 编写。 MI_KEYDEF 是 myisamdef.h 中 keydef 的对应结构。它是针对每个索引出现的多次出现结构。
- recinfo：recinfo 由 mi_open.c、mi_recinfo_write() 写入。 MI_COLUMNDEF 是myisamdef.h 中recinfo 的对应结构。它是一个多次出现的结构，在键中出现的每个字段中出现一次。

### 关键值###

MySQL 中的页面称为块。键值在块中。一个块仅包含来自一个索引的信息。每个键包含所有列的全部内容。正常的块长度为 0x0400 (1024) 字节。对于包含序号行号的固定行表，指针具有固定大小（4 字节）的数字。如果键为空，则字节为 0x00。一个普通的块至少有 65% 的空间，通常是 80% 的空间。

myisamdef.h 文件包含以下以常量表示的信息。键的最大数量为 32 (MI_MAX_KEY)，键中的最大段数为 16 (MI_MAX_KEY_SEG)。密钥的最大长度为 500 (MI_MAX_KEY_LENGTH)。块的最大长度为 16384 (MI_MAX_KEY_BLOCK_LENGTH)。

## 参考 ＃＃

- [.MYI 文件](https://dev.mysql.com/doc/internals/en/the-myi-file.html)

