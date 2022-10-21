{
  "date" : "2019-10-11",
  "keywords" :["cs","文件","扩展名","文件格式","CSharp","编程语言"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CS - CSharp 代码文件",
  "description":"了解 CS 文件格式和可以创建和打开 CS 文件的 API。",
  "linktitle" : "CS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .cs 文件？

扩展名为 .cs 的文件是 C# 编程语言的源代码文件。该文件格式由 Microsoft 引入以与 .NET Framework 一起使用，为编写代码提供了低级编程语言，该代码经过编译以生成 EXE 或 DLL 形式的最终输出文件。这些可以使用 Microsoft Visual Studio 创建和编译。 Microsoft Visual Studio Express 也可用于创建和更新此类文件，这是一个免费的 IDE。 CS 文件用于应用程序开发，范围从简单的桌面应用程序到更复杂的程序。使用 C# 语言创建的简单 Visual Studio 项目 [解决方案](/zh/programming/sln/) 可以包含一个或多个此类文件。标记为包含在编译中的文件列在 [CSPROJ](/zh/programming/csproj/) 文件中，该文件是项目的一部分，并告诉编译器使用标记的文件。

## CS文件格式##

CS 文件是基于文本的文件格式，可以在任何文本编辑器中打开以进行编辑。但是，当在支持的 IDE 中以适当的语法突出显示打开时，代码很容易阅读和排列。一个简单的 CS 文件包含：

* 命名空间声明 - 用于引用由该特定命名空间定义的特定功能
* 变量声明 - 为特定实现声明类级变量
* 方法声明 - 为特定功能声明方法声明

＃＃＃ 句法 ＃＃＃

* 分号用于表示语句的结束。
* 大括号用于对语句进行分组。语句通常分为方法（函数），方法分为类，类分为命名空间。
* 变量使用等号分配，但使用两个连续的等号进行比较。
* 方括号与数组一起使用，既可以声明它们，也可以在其中一个给定索引处获取值。

＃＃＃ 例子 ＃＃＃

```
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Hello, world!");
}
}
```

