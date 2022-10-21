{
  "date" : "2019-10-11",
  "keywords" :["vb","文件","扩展名","文件格式","Visual Basic","编程指南"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VB - Visual Basic 代码文件",
  "description":"了解 VB 文件格式和可以创建和打开 VB 文件的 API。",
  "linktitle" : "VB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .vb 文件？

VB 文件是用 Visual Basic 语言创建的源代码文件，由 Microsoft 创建，用于开发 .NET 应用程序。另一种具有不同语法的类似语言是 C#，其文件以 [.CS](/zh/programming/cs/) 文件扩展名保存。文件格式提供了用于编写代码的低级编程语言，这些代码被编译以生成 EXE 或 DLL 形式的最终输出文件。这些可以使用 Microsoft Visual Studio 创建和编译。 Microsoft Visual Studio Express 也可用于创建和更新此类文件，这是一个免费的 IDE。使用 VB 语言创建的简单 Visual Studio 项目 [解决方案](/zh/programming/sln/) 可以包含一个或多个此类文件。标记为包含在编译中的文件列在 [CSPROJ](/zh/programming/csproj/) 文件中，该文件是项目的一部分，并告诉编译器使用标记的文件。

## VB 文件格式 - 更多信息

VB 文件是基于文本的文件格式，可以在任何文本编辑器中打开进行编辑。但是，当在支持的 IDE 中以适当的语法突出显示打开时，代码很容易阅读和排列。一个简单的 VB 文件包含：

* 命名空间声明 - 用于引用由该特定命名空间定义的特定功能
* 变量声明 - 为特定实现声明类级变量
* 方法声明 - 为特定功能声明方法声明

## VB 文件格式示例

```
Imports System
Module Module1
   'This program will display Hello World
   Sub Main()
      Console.WriteLine("Hello World")
      Console.ReadKey()
   End Sub
End Module
```



