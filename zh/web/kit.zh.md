{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 KIT 文件格式和可以创建和打开 KIT 文件的 API。",
  "title" :"KIT 文件格式 - CodeKit 文件",
  "linktitle" : "KIT",
  "menu" : {
    "docs" : {
"identifier":"web-kit",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## 什么是一 .kit 文件？

带有 .kit 扩展名的文件是使用 [CodeKit](https://codekitapp.com/) 编程语言应用程序创建的 HTML 文件。除了现有的 [HTML](/zh/web/html/) 文件之外，它还包含 `imports` 和 `variables`，非常适合静态站点。 CodeKit 将 KIT 文件编译成 HTML，可以很容易地用作静态网站文件。

## 套件文件格式

KIT 文件是另外包含导入和变量的 HTML 文件。这些文件存储为纯文本文件，可以使用任何文本编辑器或 Web 文件编辑器打开。

### KIT 文件导入

几乎任何类型的文件都可以导入到 Kit 文件中。以下是将文件导入 .kit 文件的导入语法。

```
<!-- @import "someFile.kit" -->
<!-- @import "file.html" -->
```

将导入添加到 KIT 文件并保存后，它会替换为正在导入的文件的文本。您也可以使用@include 代替@import。

### KIT 文件中的多个导入

您还可以使用逗号分隔的列表一次导入多个文件：

```
<!-- @import someFile, otherFile.html, ../thirdFile.kit -->
```

## 参考

* [什么是工具包？](https://codekitapp.com/help/kit/)

