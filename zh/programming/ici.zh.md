{
  "date" : "2021-09-13", 
  "keywords" :[ "ici","文件","扩展","文件格式","ICI 实现","编程指南","ici 示例","ICI 编程语言","ICI 模块","ICI 数据模型", "ICI 文档", "ICI 语言"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICI - 编程语言文件",
  "description":"了解 ICI 文件格式和可以创建和打开 ICI 文件的 API。",
  "linktitle" : "ICI",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-13"
}

## 什么是一 .ici 文件？

一种通用的编程语言，它被解释并包含一些特性，比如动态类型以及灵活的数据类型，被称为 ICI（不是首字母缩写词）编程语言。它被认为类似于 [Perl](/zh/programming/pl/) 语言。这种 ICI 语言包含流控制结构，还包含 C 语言的一些运算符。它不是一种面向对象的语言，但 OOP 的某些特性可以通过称为上层结构的特定继承方法来实现。与 [C](/zh/programming/c) 类似，这种 ICI 编程语言具有相同的系统接口和内置函数的标准库。


## 历史简介 ＃＃

在 1980 年代后期，它由 Tim Long 开发为一种通用的解释性编程语言。这种语言的大部分特性与C相似，也可以通过应用一些特殊的方法来实现其中的一些特性。这种语言作为公共领域所有，可以作为可转售的语言使用，没有人必须提及他从哪里获得源代码。 ICI 的文档版权归 Canon Information System Research Australia 所有。

## 技术规格##

该语言中使用了两种不同的数据类型。这两个是原始数据类型和聚合数据类型。根据它们在语言中的预定义组成，这两者都包括不同的表达方式。该语言支持不同的模块，例如嵌套和子例程。由于它的某些属性与 Perl 相似，因此它与正则表达式有严格的集成。

集合仅限于异构和嵌套。这些集合为常用的集合操作（例如 Union 和 Intersection 等）提供支持。它主要用作一种语言，用于跨国组织拥有的应用程序的核心实现。

几乎所有类型的程序都可以用这种语言编写，并且大多数涉及复杂数据结构的特定程序都是用 ICI 编程语言编写的。应用程序可以以应该在其中编写的方式涉及 ICI 实现。应用程序的功能部分可以由 ICI 的模块实现。 ICI 的语言有点类似于 C 语言，但 ICI 的数据模型层次更高，并且与字典（结构）、集合、动态数组、正则表达式和（真实）字符串等类型不同。


## ICI 文件格式示例 ##

```

printf("Hello world.\n");

```

```
s = [set 200, 300, "a string"];
if (s[200])
	printf("200 is in the set\n");
if (s[400])
	printf("400 is in the set\n");
if (s["a string"])
	printf("\"a string\" is in the set\n");
s[200] = 0;
if (s[200])
	printf("200 is in the set\n");

```

```

forall (colour in [array "red", "green", "blue"])
	printf("%s\n", colour);

```

## 参考 ＃＃

* [ICI 编程语言](http://atrn.org/ici/doc/ici.html)



