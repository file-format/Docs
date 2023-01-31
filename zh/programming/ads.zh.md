
{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADS 文件 - Ada 规范文件格式",
  "description":"通过示例和可以创建和打开 ADS 文件的 API 了解什么是 ADS 文件格式。",
  "linktitle" : "ADS",
  "menu" : {
    "docs" : {
      "identifier": "programming-ads",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## 什么是 .ads 文件？

ADS 文件是 Ada 编程项目的规范文件。它类似于 Java 的类，或 C++ 的标头和实现对。 Ada 包的公共和私有规范存储在.ads 文件中。相比之下，.adb 文件包含实现或 Ada 主体。与 [C++](/zh/programming/cpp/) 一样，Ada 提供独立于 OOP 的规范和实现之间的分离。

ADS 文件可以在任何文本编辑器中打开，例如 Microsoft Notepad、Notepad++ 和 Atom。

## 广告文件格式

ADS 文件采用简单的纯文本文件格式，可以使用任何文本编辑器打开/编辑。 Ada 包可以组织成层次结构。可以通过以下方式声明子单元：

```
-- root-child.ads

package Root.Child is
   --  package spec goes here
end Root.Child;

-- root-child.adb

package body Root.Child is
   --  package body goes here
end Root.Child;

```

## 参考

* [Ada 包](https://learn.adacore.com/courses/Ada_For_The_CPP_Java_Developer/chapters/07_Packages.html)

