{
  "date" : "2020-01-10",
  "keywords" :[ "c", ".c","什么是ac文件","如何打开c文件","扩展名","文件","c文件","c文件格式","c文件扩展名"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"C - C 语言编程文件",
  "description":"了解 C 文件格式和可以创建和打开 C 文件的 API。",
  "linktitle" : "C",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-01-10"
}

## 什么是 .c 文件？

以 c 文件扩展名保存的文件是用 C 编程语言编写的源代码文件。 **C 文件** 以源代码的形式包含应用程序功能的所有实现。源代码的声明写在以 [.h](/zh/programming/h/) 扩展名保存的头文件中。 C++ 是 C 语言的现代形式，现在用于开发大多数软件。

## 历史简介

C 语言是由于为 UNIX 操作系统创建不同的实用程序而产生的。 Denis Ritchie 是创建这种编程语言的幕后推手，这项工作最初始于 1960 年代和 1970 年代初。

## C 文件格式

C 文件按照编程语言语法以纯文本文件格式编写。一个典型的 C 文件将具有：

* 文件顶部的 import 语句以导入任何头文件
* 一种或多种实现所需功能的方法

### 标头导入

扩展名为 .h 的头文件包含必要的包含语句，用于在项目中包含其他功能文件。此外，这些包含在实现文件中定义的方法的声明。使用 include 语句包含头文件，如下所示。

```
#include <filename.h>
```

### 源码实现

功能需求的实际实现被编码为 C 文件中的方法。 C 文件中的每个方法都有一个返回类型、方法名称，并且可能有一些输入参数。如果返回类型不是 void，则该方法可能会返回一些值。

### C 代码示例
这是ac示例程序：

```
long some_function();
/* int */ other_function();

/* int */ calling_function()
{
    long test1;
    register /* int */ test2;

    test1 = some_function();
    if (test1 > 0)
          test2 = 0;
    else
          test2 = other_function();
    return test2;
}
```



## **参考** ＃＃

* [类实现 - 维基百科](https://en.wikipedia.org/wiki/Class_implementation_file)

