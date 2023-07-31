{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".h","什么是 ah 文件","如何打开 h 文件","扩展名","文件","h 文件","h 文件格式","h 文件扩展名", "H 文件示例"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"H - C/C++ 头文件格式",
  "description":"了解 H 文件格式和可以创建和打开 H 文件的 API。",
  "linktitle" : "H",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## 什么是 .h 文件？

以 **h 文件扩展名** 保存的文件是 C/C++ 文件中用于包含变量、常量和函数的声明的头文件。这些由包含这些函数的实际实现的 [C++](/zh/programming/cpp/) 实现文件引用。 .h 头文件还可以包含附加信息，例如宏定义。这些头文件在 C/C++ 文件中使用 `#include` 指令引用。

一个新的 C++ 项目通常包含一个名为 **stdafx.h** 的特殊头文件，它是所有编译链的起点，所有头文件都可以包含在这个文件中。 .h 文件可以用任何文本编辑器、Eclipse IDE、Microsoft Visual Studio IDE、Borland C++ 编译器和许多其他应用程序打开。

## .H 文件格式

.h 文件是纯文本文件，它有自己的语法定义规则。头文件可以包含以下信息。

**`变量`** - 在面向对象编程 (OOP) 的情况下，类头文件包含所有类级别变量的定义，这些变量可通过实现源代码文件访问
**`方法声明`** - 所有方法声明都包含在 .h 头文件中，可以跨多个实现文件访问。
**`非内联函数定义`** - 头文件也可以包含非内联方法的定义。
**`消息映射`** - 在 MFC 源代码实现的情况下，头文件还可以包含消息映射。在这种情况下，消息映射链接到功能实现，该功能实现链接到 UI 元素，例如按钮、复选框、单选按钮等。


### 标头守卫

由于添加其他头文件，头文件可能会引发复杂错误，其中多个声明包含在同一文件中。这种重复的定义会引发编译器错误。这种有问题的情况可以通过称为标头保护的机制来避免，该机制是条件编译指令，如下所示。

```
#ifndef ANY_UNIQUE_NAME_HERE
#define ANY_UNIQUE_NAME_HERE

// your declarations (and certain types of definitions) here

#endif
```
使用此标头，预处理器检查是否已经定义了“ANY_UNIQUE_NAME_HERE"。如果标头重复包含在同一个文件中，则标头的内容将被忽略。

## H 文件示例

```
// sample.h
#pragma once
#include <vector> // #include directive
#include <string>

namespace N  // namespace declaration
{
    inline namespace P
    {
        //...
}

    enum class colors : short { red, blue, purple, azure };

    const double PI = 3.14;  // const and constexpr definitions
    constexpr int MeaningOfLife{ 42 };
    constexpr int get_meaning()
    {
        static_assert(MeaningOfLife == 42, "unexpected!"); // static_assert
        return MeaningOfLife;
}
    using vstr = std::vector<int>;  // type alias
    extern double d; // extern variable

#define LOG   // macro definition

#ifdef LOG   // conditional compilation directive
    void print_to_log();
#endif

    class my_class   // regular class definition,
    {                // but no non-inline function definitions

        friend class other_class;
    public:
        void do_something();   // definition in my_class.cpp
        inline void put_value(int i) { vals.push_back(i); } // inline OK

    private:
        vstr vals;
        int i;
    };

    struct RGB
    {
        short r{ 0 };  // member initialization
        short g{ 0 };
        short b{ 0 };
    };

    template <typename T>  // template definition
    class value_store
    {
    public:
        value_store<T>() = default;
        void write_value(T val)
        {
            //... function definition OK in template
    }
    private:
        std::vector<T> vals;
    };

    template <typename T>  // template declaration
    class value_widget;
}
```

## 参考

* [头文件管理器 - Microsoft](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

