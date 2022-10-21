{
  "date" : "2022-04-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MM 文件格式 - Objective-C++ 源文件",
  "description":"了解 XCode 中的 MM 文件以及可以创建和打开 MM 文件的 API。",
  "linktitle" : "MM",
  "menu" : {
    "docs" : {
      "identifier":"programming-mm",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-10"
}

## 什么是一 .mm 文件？

MM 文件是可以包含 Objective-C 和 Objective-C++ 编程代码的源代码文件。它用于 MacOS，与仅包含 Objective-C 代码的 .M 文件不同。当编译器看到 .mm 扩展名时，它能够编译文件中存在的 C++ 类。由于单个源代码文件可以包含 [C](/zh/programming/c/) 和 [C++](/zh/programming/cpp/) 语言的混合，将 .m 文件重命名为 .mm 扩展名允许 C++ 功能设置可以打开 .MM 文件的应用程序包括 Apple TextEdit、Microsoft Notepad、Notepad++ 和 Microsoft Wordpad。

## 参考

* [iOS 项目导入错误](https://developer.apple.com/forums/thread/92931)

