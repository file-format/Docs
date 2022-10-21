{
  "date" : "2019-10-11",
  "keywords": [ "M file", "M", "extension", "format", "M file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M - Matlab 源代码文件",
  "description":"了解 Matlab .m 源代码文件和可以创建和打开 MF 文件的 API。",
  "linktitle" : "M",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

# M - Matlab 源代码文件

## 什么是 M (Matlab) 文件？

扩展名为 .m 的文件是 Matlab 使用的源代码文件，Matlab 是一种用于分析、算法开发和仿真建模的编程和数值计算平台。与其他编程文件格式一样，M 文件包含执行 Matlab 命令以绘制图形、运行模拟和其他数学运算的源代码。单个 Matlab 仿真可以跨越多个这样的 .m 文件，这些文件可以将应用程序分类为脚本、类、函数或声明。 Matlab M 文件可以用任何文本编辑器打开。

## Matlab M 文件格式 - 更多信息

Matlab .m 文件是包含 Matlab 编程语言的编程代码的文本文件。这些可以在任何文本编辑器中打开和编辑，并保存回来以在 Matlab 软件中执行。 Matlab 本身包含一个实时编辑器，用于创建包含代码、输出和格式化文本的脚本。

### Matlab 函数文件

与其他编程语言一样，您可以创建一个仅包含仅执行特定任务的函数定义的 .m 文件。此类文件也以 .m 扩展名保存，并且仅实现与该功能相关的功能。

### .M 文件示例

下面是一个 Matlab 函数文件示例，用于计算物体从高度 h 落下所需的时间。

```C++
function t= TimeToGround(h)  
  t=sqrt(h/4.9);
end
```

要从 Matlab 编辑器或另一个 .m 文件调用此函数，可以使用以下代码。
```C++
TimeToGround(100)
```

## 参考

* [Matlab - 支持的文件格式](https://www.mathworks.com/help/matlab/standard-file-formats.html)
* [使用 Matlab](https://www.maths.unsw.edu.au/sites/default/files/MatlabSelfPaced/lesson0/MatlabLesson0_Mfiles.html)

# M - Objective-C 实现文件

## 什么是 M (Objective-C) 文件？

M 文件也称为实现文件，其中包含用 Objective-C 语言编写的类的源代码，Objective-C 是一种用于为 OS X 和 iOS 编写软件应用程序的编程语言。 Objective-C 是 Apple 的主要 API、Cocoa 和 Cocoa Touch 用于这些平台的主要编程语言。用这种语言开发的单个软件应用程序可能包含多个 .m 文件，其中包含程序类的实现。这些可以使用 Apple XCode、jEdit 和其他常用文本编辑器打开。

## Objective-C M 文件格式 - 更多信息

M 文件使用 Objective-C 的编程语法以纯文本格式编写。类的每个方法都必须在这些实现文件中定义其所有必要的代码。这些实现M文件可以根据需要导入一个或多个.h头文件。 import 语句告诉编译器在哪里可以找到属于这个实现文件的头文件。导入语句编写如下。

```C++
#import "network.h"
```

然后每个 M 文件实现都以 `@implementation` 指令开头，后跟实现类文件名。然后是在头文件中声明的所有方法实现。

### M 文件格式示例

```C++
UrlConnection.m

#import "UrlConnection.h"

@implementation UrlConnection

(void)connect {
    // In here would be code to attempt a connection to the
    // specified URL, while possibly handling connection errors.
    //
}

 + (BOOL)canHandleRequest:(NSString \*)type
                   forUrl:(NSString \*)url {
    //And in here would be code to see if the given URL passed
    // in is capable of handling the HTTP request type specified
    // by the "type" parameter. It will return YES or NO.
 }

 @end
```

## 参考
* [关于目标 C](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html#//apple_ref/doc/uid/TP40011210-CH1-SW1)
* [Object-C 指南](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

