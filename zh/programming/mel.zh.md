{
  "date" : "2019-10-11",
  "keywords" :[".mel","Maya 嵌入式语言","文件","扩展名","文件格式","Maya 3D","编程指南"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MEL - Maya 嵌入式语言文件格式",
  "description":"了解 MEL 文件格式和可创建和打开 MEL 文件的 API。",
  "linktitle" : "MEL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-03-08"
}

## 什么是一 .mel 文件？

扩展名为 .mel（Maya 嵌入式语言）的文件是 Autodesk Maya 用于创建图形界面的脚本语言。除了 Maya 的图形界面外，它还允许您使用可执行脚本自动创建图形元素。 MEL 使您无需学习编程即可创建图形界面。这是通过创建加速重复任务的宏和自定义操作来实现的。这些程序和脚本让您可以创建自定义建模、动画、动态和任务渲染。 Autodesk Maya 2020 可用于打开和查看 EML 文件的内容。

## MEL 文件格式 - 更多信息

程序员的 [参考手册](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865) 在 Maya 的文档部分可供开发人员使用。 MEL 是基于 shell 脚本命令，类似于 UINX 来实现的。基于脚本的命令使其与传统的和面向对象的编程 (OOP) 无关，导致不使用数据结构、调用函数或使用其他语言中的 OOP。

关于 MEL 的一些关键点如下。

`Comments` - MEL 中的每个语句都必须以分号 (;) 结尾，即使在块的末尾也是如此。

`Returning Values` - 声明返回值的表达式不会自动打印 MEL 中的值。相反，它会导致错误。
```
3 + 5;
// Error: 3 + 5; //
// Error: Syntax error //
print(3+5);
8
```
`用于创建、编辑和删除的命令` - 相同的命令用于创建事物、编辑事物或查询有关现有事物的信息。但是，标志控制命令的作用（创建、编辑或查询）。

```
// Create a sphere named "mySphere" with radius 5
sphere -radius 5 -name "mySphere";
// Edit the radius of mySphere
sphere -edit -radius "mySphere";
// Print the radius of mySphere
sphere -query -radius

```
`Return Value from Function` - 函数语法自动返回一个值。要使用命令语法获取返回值，您必须将命令括在反引号中。

```
$a = getAttr("mySphere.translateX"); // Function syntax
$b = `getAttr mySphere.translateY`; // Command syntax
```

## 参考

* [MEL](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865)

