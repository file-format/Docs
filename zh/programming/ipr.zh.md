{
  "date" : "2021-09-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IPR 文件格式 - IntelliJ IDEA 项目文件",
  "description":"了解 IPR 文件格式和可以创建和打开 IPR 文件的 API。",
  "linktitle" : "IPR",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-13"
}

## 什么是一 .ipr 文件？

IPR 文件是使用 Java IDE **IntelliJ IDEA** 创建的项目文件。所有与项目设置相关的信息，例如目录结构、源代码文件、项目中包含的库和编译器设置都存储在 IPR 文件中。从 IntelliJ IDEA 中打开项目时，IDE 会读取 IPR 文件中的信息并加载相应的文件和设置。 IPR 文件已替换为 .IDEA 文件，其中包含作为设置目录的所有信息。

## 知识产权文件格式

IPR 文件以人类可读的普遍可理解的 [XML](/zh/web/xml/) 文件格式保存。它包含标签中的所有项目相关信息，这些标签为显示项目相关内容而加载。

由于 IPR 文件以 XML 文件格式存储，因此可以在任何文本编辑器中打开这些文件，例如 Notepad、Notepad++、Atom 和 Apple TextEdit。

## 参考 ＃＃

* [创建管理项目 - IntelliJ IDEA](https://www.jetbrains.com/help/idea/creating-and-managing-projects.html)

