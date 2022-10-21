{
  "date" : "2021-07-23",
  "keywords" :["PL","文件","扩展","格式","Perl","Perl 语言","PL 文件","编程"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 PL 文件格式和可以创建和打开 PL 文件的 API。",
  "title" :"PL 文件 - Perl 脚本文件格式",
  "linktitle" : "PL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-07-23"
}

## 什么是一 .pl 文件？

扩展名为 .pl 的文件是一种 Perl 脚本文件，它是一种脚本语言。这些是使用 Perl Interpreter 软件编译和运行的。 PL 脚本文件包含代码行、变量和注释。脚本语言比较难
了解其他编程文件格式，例如 [PHP](/zh/programming/php/)。 PL 文件可以创建并与 Windows、macOS 和 Linux 兼容。

## Perl 脚本语言简史

该语言于 1987 年首次使用，因此这些文件起源于那一年。 1989 年，Perl 2 发布。后来又更新了，一直修改到5.35版本，下个版本目标是明年发布。

在每次更新中，都添加了有关语言和文件的功能、性能和外观的工具。这些年对版本进行了多次修改。它最初是一种基本的脚本语言，但现在它也包含许多其他模块。本来它是一种很简单的语言，但是这种语言的文字很紧凑，很难理解。

## Perl 文件格式扩展规范

这些编程文件有一些属性或规范，其中一些如下：

* 这些文件中包含的代码为纯文本格式，用于脚本开发
* 服务器脚本、文本解析和服务器管理是该语言脚本涵盖的主要方面
* 与该语言相关的许多流行程序是 Active state Active Perl 和 Bare Bones BBEdit（与 Mac OS 兼容）
* 这种语言被认为是高级语言
* 对于 Win32，用户可能需要安装该语言的本机二进制发行版
* 它需要一些脚本工具才能在各种 Windows 资源工具包中执行
* Visual Studio .NET 是用于开发编程语言的著名框架。称为 Visual Perl 的 Active State 工具用于将 Perl 添加到 Visual Studio
* 在文件中，源代码的第一行描述了正在使用的解释器的信息。 PL 文件通常以 **#!/usr/bin/perl** 行开头，告诉您的计算机使用安装在计算机中的 Perl 解释器运行此脚本


## PL 脚本示例

```
#!/usr/bin/perl
print "Hello, world\n";
```

这将打印

```
Hello, World
```

### 单行注释###

```
#!/usr/bin/perl
# This is a single line comment
print "Hello Perl\n";
```

### 多行注释###

```
#!/usr/bin/perl
=begin comment
This is a multiline comment.
Line 1
Line 2
=cut
print "Hello Perl\n";
```

### 变量赋值###

```
#!/usr/bin/perl
$a = 10;
print "Variable a = $a\n";
```

### 标量变量赋值###

```
#!/usr/bin/perl
$age = 35; # Assigning an integer
$name = "Tony Stark"; # Assigning a string
$pi = 3.14; # Assigning a floating point
```

### 简单的标量操作###

```
#!/usr/bin/perl
$constr = "hi" . "perl";# Concatenates two or more strings.
$add = 40 + 10; # addition of two numbers.
$prod = 4 * 51;# multiplication of two numbers.
$connumstr = $constr . $add;# concatenation of string and number.
```

## 参考 ＃＃

- [Python (编程语言) - 维基百科](https://en.wikipedia.org/wiki/Python_(programming_language))

