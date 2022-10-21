{
  "date" : "2019-10-11",
  "keywords" :["c++","文件","扩展名","文件格式","C++","编程语言"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPP - C++ 源代码文件",
  "description":"了解 CPP 文件格式和可以创建和打开 CPP 文件的 API。",
  "linktitle" : "CPP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是 C++ 文件？

具有 CPP 文件扩展名的文件是以 C++ 编程语言编写的应用程序的源代码文件。单个 C++ 项目可能包含多个 CPP 文件作为应用程序源代码。这样的项目由不同的文件类型组成，其中 CPP 文件被称为实现文件，因为它们包含头文件 (.h) 中声明的方法的所有定义。当作为一个整体编译时，C++ 项目作为一个整体会产生一个可执行的应用程序。

## CPP 文件结构

与头文件相比，CPP 文件结构简单。这种实现文件的主要目的是将接口与实现分开。这导致在头文件中声明所有成员函数，并在 CPP 文件中声明它们的详细信息。 CPP 实现文件可以用作编写应用程序的简单文件或用作类实现。

### 独立实现

当作为一个独立的应用程序使用时，一个 CPP 文件可以包含其中的所有实现，而不需要在头文件中声明方法。这样的实现由实现文件中定义的所有方法组成，其中应用程序的条目由将可选用户输入作为参数的主方法控制。它还可以包含 C++ 标准库中的任何库，以供文件中任何声明的方法使用。

```
/*
* File: main.cpp
* Author: SomeOne
* Created on November 16, 2018, 4:09 PM
*/

#include <iostream>
using namespace std;

int main()
{
   cout<<"About the CPP file format";
   cout<<std::endl<<"and its very easy";
}
```

### 类实现

在面向对象编程 (OOP) 中，CPP 文件用作类定义。在这种情况下，所有的类数据成员和成员函数都在头文件中声明。每个头文件也可以依次引用标准库方法。类定义 CPP 文件引用文件开头包含语句中的头文件。大多数情况下，软件开发人员在此类实现文件的开头包含注释，提供有关文件实际内容、作者详细信息和实现日期的信息。在这种情况下，头实现文件必须具有相同的名称。这种头文件和实现文件的示例如下。

### 头文件

```
#include <string>
#include <iostream>

using namespace std;

class MyClass {
public:
   MyClass();     // Constructor
   void add(int i, int j);

private:
   std::string name;
};
```

### CPP 实施文件

```
#include "MyClass.h"

MyClass::MyClass(){
   ...
}
void MyClass::add(int i, int j) {
   int result # i + j;
}
```

## 参考

* [类实现 - 维基百科](https://en.wikipedia.org/wiki/Class_implementation_file)

