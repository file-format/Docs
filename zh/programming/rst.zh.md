{
  "date" : "2022-04-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RST 文件格式 - reStructuredText 文件",
  "description":"了解 RST 文件格式和可以创建和打开 RST 文件的 API。",
  "linktitle" : "RST",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-11"
}

## 什么是一 .RST 文件？

RST 文件是一种技术文档文件格式，主要用于 Python 编程社区。它是用 reStructuredText 标记语言编写的文本文件，它将样式和格式应用于纯文本文档以生成文档。 RST 文件使用 Python 程序代码中的注释和其他信息来创建应用程序的技术文档。但是，这些也可以包含可以转换为简单网页和 [eBooks](/zh/ebook/) 的文本。 Github Atom、GNU Emacs（跨平台）、Microsoft Notepad (Windows)、Apple TextEdit (Mac) 和 Vim (Linux) 等文本编辑器可用于打开 RST 文件。

## RST 文件格式

RST 文件包含用 reStructuredText 标记语言编写的代码。它是 Python Doc-SIG（文档特别兴趣小组）的 Docutils 项目的一部分，该项目为 Python 提供了一组类似于 Javadoc for Java 的工具。 RST 文件格式的解析器嵌入在 Docutils 中，可以从 Python 程序中提取信息以将其格式化为程序文档。

### reStructuredText RST 示例

让我们以 RST 文件格式编写的示例文本如下。

```
================
Document Heading
================

Heading
=======

Sub-heading
-----------

Paragraphs are separated
by a blank line.
```

当此文本输入到 rST 处理器（如 Docutils）时，输出如下。

```
<h1>Document Heading</h1>

<h2>Heading</h2>

<h3>Sub-heading</h3>

<p>Paragraphs are separated
by a blank line.</p>
```

## 参考 ＃＃

* [reStructuredText - 维基百科](https://en.wikipedia.org/wiki/ReStructuredText)

