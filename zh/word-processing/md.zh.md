{
  "date" : "2019-10-11",
  "keywords" :["md 文件","md 文件格式","什么是 md 文件","文件","md 示例","md 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MD - MarkDown 语言文件",
  "description":"了解 MD 文件格式和可以创建和打开 MD 文件的 API。",
  "linktitle" : "MD",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .md 文件？

使用 Markdown 语言方言创建的文本文件以 **.md** 或 **.MARKDOWN** 文件扩展名保存。 MD 文件以使用 Markdown 语言的纯文本格式保存，该语言还包括内联文本符号，定义如何格式化文本，例如缩进、表格格式、字体和标题。 MD 文件可以使用 Markdown 程序转换为 HTML。 Markdown 语言由 John Gruber 发布。

MD 文件也可以归类为 Markdown 主要使用的开发人员文件，用于将文本文件转换为 HTML 版本，以便用户可以创建易于阅读和编写的文件。以下是可以打开 .md 文件的应用程序：

* 微软记事本
*记事本2
* 苹果文本编辑
* 微软写字板

请注意，不要重命名 .md 文件的扩展名。如果是这样，这不会更改文件类型，因为有特殊的转换软件可用于将文件从一种类型更改为另一种类型。如上所述，.MD 文件是 Markdown 语言软件创建的文件的扩展名。 **Markdown** 是一种 [轻量级标记语言](https://en.wikipedia.org/wiki/Lightweight_markup_language)，旨在用于使用纯文本格式化语法来格式化网络上的文本。明确一点，Markdown 不是 HTML 的替代品，因为它的语法非常小，只包含非常小的 HTML 标记子集。 Markdown 背后的原因是为了便于阅读、编写和编辑散文。换句话说，我们可以说 HTML 是一种发布格式，而 Markdown 是一种写作格式。

Markdown 现在是世界上最流行的标记语言之一。在使用 Microsoft Word 时，可以通过单击按钮来格式化单词和短语，并且可以立即看到更改。但 Markdown 不是这样的。创建 Markdown 格式文件时，会将 Markdown 语法添加到文本中，以指示哪些单词和短语可能看起来不同。例如，为了显示一个标题，在它之前添加一个数字符号（例如# Heading One）。为了制作一个粗体句子，在它之前和之后添加两个星号（例如，**此文本是粗体**）。在正文之后可以看到 Markdown 语法。

## 历史简介

John Gruber 和 Aaron Swartz 在 2004 年创建了 Markdown 语言，其理念是让人们“使用易于阅读和编写的纯文本格式进行书写，并可选择将其转换为 XHTML 或 HTML。其设计背后的目标是可读性 - 语言是可读的，而不是看起来像在 RTF 或 HTML 等标记语言中那样标记或添加了格式化指令，其中标记和格式化指令是显而易见的。基本灵感是使用现有的惯例来标记电子邮件中的纯文本。

从那时起，其他人重新实现了 Markdown，就像在 [CPAN](https://en.wikipedia.org/wiki/CPAN) 上提供的 Perl [模块](https://en.wikipedia.org/wiki/Modular_programming) 中一样 和其他各种编程语言。它是根据 [BSD 风格的许可证](https://en.wikipedia.org/wiki/BSD_license) 分发的，并且包含在多个 [内容管理系统](https://en.wikipedia.org/wiki/Content_management_system)。

## 技术规格

使用 Markdown 编写内容时，首先将文本存储在扩展名为 .md 或 .markdown 的纯文本文件中，然后使用诸如 Dillinger 之类的 Markdown 应用程序处理 Markdown 文件，将 Markdown 格式的文本转换为 HTML 以在 Web 中显示浏览器。 Markdown 应用程序使用 //Markdown 处理器//（通常也称为“解析器"或“实现"）来获取 Markdown 格式的文本并将其输出为 HTML 格式。该过程的流程图如下：

简而言之，它是一个四步过程，如下所示：

1. 首先，使用文本编辑器或扩展名为 .md 或 .markdown 的 Markdown 应用程序创建 Markdown 文件。
1. 然后在 Markdown 应用程序中打开 Markdown 文件。
1. Markdown 应用程序用于将 Markdown 文件转换为 HTML 文档。
1. 然后在网络浏览器中查看 HTML 文件或使用 Markdown 应用程序将其转换为另一种文件格式，如 PDF。

Markdown 可以快速轻松地记笔记、为网站编写内容、生成可打印的文档、出版书籍、生成演示文稿和制作文档。

markdown 中的一些版本对其他版本产生了重大影响，以至于人们经常会看到它们被引用为其他版本的一部分。例如，图书馆提到了对 CommonMark (GFM) 的支持。让我们简要看看这些。

### GFM
Markdown 在开发人员中如此受欢迎，因为开源共享平台 Github 接受并使用称为 Github Flavored Markup (GFM) 的版本扩展了该语言，其中包括围栏代码块、URL 自动链接、删除线、表格和创建待办事项。

### 通用标记
Markdown 开发人员最近尝试标准化 Markdown，他们联合起来为更强大的语言创建版本、测试和文档，称为 CommonMark。这种格式有点新，不支持很多功能，但很快就会添加很多 MultiMarkdown 功能。

### 多降价
Multi-Markdown 为该语言添加了其他版本支持的各种功能。最初它是用 Perl 编写的，但后来转移到 C。它支持围栏代码块、语法突出显示、表格、元数据、片段/交叉引用链接、脚注、删除线、定义列表、数学。

## 参考

* [掌握 MarkDown](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

