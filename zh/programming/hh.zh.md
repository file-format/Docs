{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".hh","什么是.hh文件","如何打开.hh文件", "扩展名", "文件", ".hh文件",".hh文件格式", " .hh 文件扩展名",".HH 文件示例"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HH - C++ 头文件格式",
  "description":"了解 HH 文件格式和可以创建和打开 HH 文件的 API。",
  "linktitle" : "HH",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-20"
}

## 什么是一 .hh 文件？

扩展名为 .hh 的文件是 C++ 头文件，其中包括变量、常量和函数的声明。这些声明由相应的 C++ 实现文件使用，通常保存为包含用户逻辑的实际实现的 [.cpp](/zh/programming/cpp/) 文件。使用 `#include` 指令在实现 CPP 文件中引用 .hh 头文件。您可以将尽可能多的头文件添加到您的 C++ 项目中以包含项目级声明。

## .HH 文件格式

.hh 文件是根据头文件定义规则创建的纯文本文件。 .hh 文件中声明的最常见信息包括以下内容。

**`变量`** - 在面向对象编程 (OOP) 的情况下，类头文件包含所有类级别变量的定义，这些变量可通过实现源代码文件访问
**`方法声明`** - 所有方法声明都包含在 .h 头文件中，可以跨多个实现文件访问。
**`非内联函数定义`** - 头文件也可以包含非内联方法的定义。
**`消息映射`** - 在 MFC 源代码实现的情况下，头文件还可以包含消息映射。在这种情况下，消息映射链接到功能实现，该功能实现链接到 UI 元素，例如按钮、复选框、单选按钮等。

## .H 和 .HH 文件之间的区别

显然，.h 和 .hh 头文件之间没有这样的区别，除了为各自的语言（即 [C](/zh/programming/c/) 或 C++）使用这些头文件的推荐方式之外。根据这些语言命名您的头文件有助于您在可能是 C 和 C++ 实现的混合的大型项目中区分这些文件。

此外，如果标题由扩展名分隔，您的编辑器可以自动分别应用适当的格式。

总体而言，这两种文件格式的区别不会造成任何伤害，而是有利的，鼓励遵循 C 和 C++ 的区别。

### 标头守卫

由于添加其他头文件，头文件可能会引发复杂错误，其中多个声明包含在同一文件中。这种重复的定义会引发编译器错误。这种有问题的情况可以通过称为标头保护的机制来避免，该机制是条件编译指令，如下所示。

```
#ifndef ANY_UNIQUE_NAME_HERE_HPP
#define ANY_UNIQUE_NAME_HERE_HPP

// your declarations (and certain types of definitions) here

#endif
```
使用此标头，预处理器检查是否已经定义了“ANY_UNIQUE_NAME_HERE_HPP"。如果标头重复包含在同一个文件中，则标头的内容将被忽略。

## 参考

* [头文件管理器 - Microsoft](https://docs.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)
* [.h 和 .hh 文件格式的区别](https://stackoverflow.com/questions/10354321/c-reason-why-using-hh-as-extension-for-c-header-files)

