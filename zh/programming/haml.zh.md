{
  "date" : "2022-04-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HAML 文件格式 - Haml 源代码文件",
  "description":"了解 HAML 文件格式和可以创建和打开 HAML 文件的 API。",
  "linktitle" : "HAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-07"
}

## 什么是一 .haml 文件？

HAML 文件是一种 HTML 抽象标记语言文件，其中包含以 [Haml](https://haml.info/) 语言编写的源代码。它可以用作 ERB（Ruby 模板脚本）的替代品。 HAML 文件包含用于生成 Web 文档的 HTML 的模板源代码。通过更改文件的扩展名，只需将 app/views 文件夹中的这些文件替换为 Haml 即可替换 ERB 文件。 HAML 文件可以使用任何文本编辑器打开，例如 Microsoft Notepad、Notepad++、Apple TextEdit、

## HAML 文件格式

HAML 文件是作为纯文本文件保存到光盘的源文件。它包含用 HAML 语法编写的代码。 HAML 将 **<>** 标记替换为 **%** 符号，以使代码更简单、更容易。 ERB 文件可以直接替换为 HAML，如以下简单示例所示。

```
app/views/account/login.html.erb → app/views/account/login.html.haml
```

### HAML 示例

以下是 HAML 的 Hello World 示例。

```
%p{:class => "sample", :id => "welcome"} Hello, World!
%p.sample#welcome Hello, World!
```
它呈现为以下 HTML 输出。

```
<p class="sample" id="welcome">Hello, World!</p>
```

## 参考

* [HAML - Github](https://github.com/haml/haml)

