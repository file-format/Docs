{
  "date" : "2022-07-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"INC 文件扩展名 - 什么是 INC 文件？",
  "description":"了解 INC 包含文件格式和可以创建和打开 INC 文件的 API。",
  "linktitle" : "INC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-07-14"
}

## 什么是一 .inc 文件？

INC 文件是一个包含文件，软件程序的源代码使用它来引用头信息。它类似于 [.h 文件格式](/zh/programming/h/) 并且包含可以被 C++ 等源代码文件重用的声明、函数、头文件或宏。 INC 文件被多种编程语言使用，例如 C、[C++](/zh/programming/cpp/)、Pascal、[PHP](/zh/programming/php/) 和 [Java](/zh/programming/java/)。 Microsoft Notepad、Notepad++ 和 TextEdit 等文本编辑器可用于打开 INC 文件。

## INC 文件格式 - 更多信息

INC 文件保存为纯文本文件，其中包含根据声明语法的所有声明。一个 INC 文件也可以引用其他 INC 文件。一旦创建，INC 文件就成为项目的一部分，并且可以从源文件（例如 C++）中引用。它可以被多个源文件引用以避免任何重复。

## INC 文件内容

INC 文件可以包含以下信息。

**`变量`** - 在面向对象编程 (OOP) 的情况下，类头文件包含所有类级别变量的定义，这些变量可通过实现源代码文件访问

**`方法声明`** - 所有方法声明都包含在 .h 头文件中，可以跨多个实现文件访问。

**`非内联函数定义`** - 头文件也可以包含非内联方法的定义。

## 在 PHP 中使用 INC 文件的缺点

PHP 是在服务器上运行并将结果返回给调用网页的服务器端脚本。如果 PHP 文件引用了 INC 文件，并且服务器没有配置为解析 .inc 文件（这很常见），用户可以通过访问 URL 目录查看 .inc 文件中的 php 源代码。因此，在 PHP 中使用 INC 文件作为包含文件时必须小心。

## 参考

* [在 PHP 中使用 INC](https://stackoverflow.com/questions/7129842/what-is-an-inc-and-why-use-it)

