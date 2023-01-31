{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AGI 文件 - Asterisk 网关接口文件格式",
  "description":"通过示例和可以创建和打开 AGI 文件的 API 了解什么是 AGI 文件格式。",
  "linktitle" : "AGI",
  "menu" : {
    "docs" : {
      "identifier": "programming-agi",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## .agi 文件是什么？

AGI 文件是开源电话系统 Asterisk 使用的脚本文件。它包含可用于自动化流程和 Asterisk 拨号方案的信息。使用 AGI 脚本文件，可以与关系数据库（如 PostgreSQL 或 MySQL）建立连接。此外，AGI 脚本也可用于访问其他外部资源。 AGI 脚本可以将拨号方案的控制权交给外部 AGI 脚本，使 Asterisk 能够执行复杂的任务。

## AGI 文件格式 - 更多信息

AGI 脚本文件保存为文本文件，可以在任何文本编辑器中打开以进行更改。

### AGI通信标准模式

AGI 脚本加载 Asterisk 发送给它的变量和它们的值。这些变量的常见外观如下。

```
agi_request: test.py
agi_channel: Zap/1-1
agi_language: en
agi_callerid:
agi_context: default
agi_extension: 123
agi_priority: 2
```

这些变量之后是 Asterisk 发送的空行，表明 AGI 脚本现在可以控制拨号方案。

### AGI 脚本文件的编程语言

AGI 脚本通常可以用 Perl、[PHP](/zh/programming/php/)、[C](/zh/programming/c/)、Pascal 或 Bourne Shell 编写。

## 参考

* [Asterisk AGI 脚本](https://www.oreilly.com/library/view/asterisk-the-future/9780596510480/ch09.html)

