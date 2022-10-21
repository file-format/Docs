---
date: 2019-10-11
keywords: "dart, .dart, dart 文件格式, dart 文件, 如何运行 dart 文件, .dart 扩展名"
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "飞镖文件格式"
linktitle: "镖"
description: "了解 Dart 文件格式和可以创建和打开 Dart 文件的 API。"
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-18
---

## 什么是一 .dart 文件？ ##

Dart 文件包含 Dart 编程语言的源代码，这是一种由 Google 开发的客户端优化编程语言，用于为移动、桌面、Web、Iot（物联网）等构建应用程序。Dart 是一种面向对象的语言使用类似于 C 的语法。 Dart 可以编译为 JavaScript 或本机代码。您可以像运行 javascript 文件一样在著名的 Web 浏览器中运行 Dart 文件。 Dart SDK 附带的称为 Dart 虚拟机的命令行工具也可用于编译和运行 Dart 文件。

## 历史简介 ＃＃

Dart 项目由 Lars Bak 和 Kasper Lund 创立，第一个版本于 2013 年 11 月 14 日发布。由于计划在 Google Chrome 中包含 Dart VM，一开始 Dart 因网络碎片化而受到批评。这些计划被放弃了，Dart 在 2015 年发布了 1.9 版，专注于编译为 JavaScript。

Dart 2.0 于 2018 年 8 月发布，其中引入了 dart2native 扩展，将 Dart 代码编译到原生 Linux、Windows、macOS 平台。此扩展启用了自包含的可执行文件，因此不需要 Dart SDK 即可在这些平台上运行 Dart 应用程序。此扩展还与 Flutter 集成，从而可以创建跨平台应用程序。

ECMA 标准化了 Dart，2014 年 7 月发布了第一版，2014 年 12 月发布了第二版。


## 如何运行/执行 Dart 代码##

Dart 代码可以通过以下方式运行：

- **编译为 JavaScript**：</br> Dart 代码使用 dart2js 编译器编译为 JavaScript。编译后的 JavaScript 代码与所有主要的 Web 浏览器兼容。
- **独立**：</br> Dart 软件开发工具包 (SDK) 附带一个独立的 Dart VM，它允许 Dart 代码在命令行界面中运行。 Dart 附带一个完整的标准库，允许用户编写功能齐全的应用程序。
- **提前 (AOT) 编译**：</br> Dart 代码可以被 AOT 编译为机器代码，允许使用 Flutter 构建移动应用程序。
- **本国的**：</br>使用 dart2native 编译器，可以将 Dart 代码编译为可在 Windows、Linux 和 macOS 上运行的独立可执行文件。

## 飞镖文件格式##

Dart 是一种 C 风格的面向对象语言，支持接口、mixin、抽象类、具体泛型和类型接口。

＃＃＃ 句法 ＃＃＃

以下是 Dart 语法的一些示例。

#### 打印到控制台####

```dart
// print "Hello World" to console
main() {
  print("Hello, World!");
}
```

#### 循环和数组####

```dart
// loops and arrays
var names = {
  'John',
  'James',
  'Rose',
};
main() {
  for (var name in names) {
    print(name);
  }
}
```

＃＃＃＃ 功能 ＃＃＃＃

```dart
// functions
int double(int x) {
  return x * 2;
}
main() {
  print("double of 10 is ${double(10)}");
}
```

#### 类####

```dart
// classes
abstract class Person {
  detail();
}

class Student implements Person {
  String firstName = "Jack";
  String lastName = "Wick";
  detail() => print("Student: $firstName $lastName");
}

main() {
  // The 'new' keyword is optional.
  Student student = Student();
  student.detail();
}
```

#### 混合####

Mixin 是普通的类，我们可以从中借用方法/变量而无需继承它们。这是通过使用 *"with"* 关键字来完成的。

```dart
class B {  
  method(){
     ....
  }
}

class A with B {
  ....
     ......
}
void main() {
  A a = A();
  a.method();  //We are able to access the method of B class without inheriting from it.
}
```

## 参考 ＃＃

- [Dart (编程语言) - 维基百科](https://en.wikipedia.org/wiki/Dart_(programming_language))
- [飞镖](https://dart.dev/)

