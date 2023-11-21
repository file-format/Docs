{
"date": "2023-05-15",
  "keywords": [
".csx 文件",
"什么是 csx 文件",
"csx 文件包含什么",
"csx文件的格式是什么",
"文件",
".csx 文件扩展名",
"扩大"
],
  "author": {
"display_name": "沙基尔·法伊兹"
},
"draft": "false",
"toc": true,
"title": "CSX 文件格式 - Visual C# 脚本",
  "description":"了解可创建和打开 CSX 文件的 CSX 格式和 API。",
"linktitle": "CSX",
  "menu": {
    "docs": {
      "identifier": "programming-csx",
"parent": "programming"
}
},
"lastmod": "2023-05-15"
}

## 什么是 .csx 文件？

Visual C# Script（也称为 CSX）是 Microsoft .NET 生态系统中 Roslyn 脚本引擎使用的一种文件格式。 CSX 文件包含可以直接执行的 C# 代码,无需单独的编译步骤。

CSX 格式是 Microsoft 生态系统特有的,并不是一般编程中广泛使用的文件格式。 CSX 文件通常用于需要快速原型设计或脚本功能的场景。与创建成熟的编译应用程序相比,它们使您能够以更轻量级的方式创建和运行 C# 程序。

要执行 CSX 文件,您可以使用 .NET Interactive Notebooks 等工具,它提供了用于运行 C# 代码的交互式环境。具有 C# 扩展和 .NET Core SDK 的 Visual Studio Code 也可用于处理 CSX 文件。

## CSX 文件包含什么？

CSX（C# 脚本）文件包含可以直接执行的 C# 代码。它可以包含任何有效的 C# 代码,例如变量声明,函数,类和其他编程结构。

以下是 CSX 文件可能包含的内容的示例：

```
using System;

// Define a class
public class MyClass
{
    public void Greet(string name)
    {
        Console.WriteLine("Hello, " + name + "!");
}
}

// Create an instance of the class and call a method
var myObject = new MyClass();
myObject.Greet("John");

```

CSX 文件还可以包含导入语句,外部库引用和其他 C# 语言功能以支持代码的功能。该代码可以即时解释和执行,无需编译,因此适合脚本编写和快速原型设计任务。

## CSX 文件的格式是什么？

CSX（C# 脚本）格式遵循简单的基于文本的格式。它通常具有文件扩展名 .csx,以区别于常规 C# 源代码文件 (.cs)。

可以使用任何支持 C# 语法突出显示的文本编辑器或集成开发环境 (IDE) 来编辑 CSX 文件。 CSX 文件准备就绪后,可以使用 .NET 交互式笔记本,.NET Core 命令行界面 (CLI) 或支持 C# 脚本的 IDE 等工具来执行它。

## 参考
* [使用 Visual Studio Code 进行 C# 编程](https://code.visualstudio.com/docs/languages/csharp)

