{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BML 文件格式 - Bean 标记语言文件",
  "description":"了解 BML 文件格式和可以创建和打开 BML 文件的 API。",
  "linktitle" : "BML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-12"
}

## 什么是一 .bml 文件？

扩展名为 .bml 的文件是一种 Bean 标记语言文件，它存储用于支持 Java 应用程序的 Java 类。这允许访问 Java 对象和方法，并且不需要使用 Java 类创建新功能。它指定组件如何相互连接以执行有用的任务。 BML 由 IBM alphaWorks 开发，用于描述结构和组件关系。可以使用任何文本编辑器（例如 Web 浏览器、Microsoft Notepad 和 Notepad++）打开和查看 BML 文件。

## BML 文件格式

IBM alphaworks 网站提供了两种 BML 实现。第一个实现是一个解释器，它“播放"一个 BML 脚本来生成所需的 bean 层次结构。第二种实现是将任何 BML 脚本编译成无反射 Java 代码的编译器。从某种意义上说，这是有利的，因为它允许使用专为此特定目的而设计的语言捕获应用程序的组件间结构，并增加了将其编译为“常规"Java 代码的能力。

## BML 标签

以下是BML语言中使用的一些标签的解释：

＃＃＃ 这<bean>标签：

这<bean>元素用于创建新 bean 或按名称查找 bean。这<bean>标签的格式为：
```
<bean class = "classname or serialized file" [id = "name"]>
</bean>
```
标记中的“id"与 JavaBean 的对象注册表相关联。

＃＃＃ 这<string>标签

字符串标签有两种使用方式：

1. 创建非空字符串：

```
<string [value = "value of string"]> [value of string]
</string>
```
2. 创建一个空字符串：

```
<string/>
```
## 参考

* [使用 XML 的面向对象的消息传递](https://docs.oracle.com/cd/A87860_01/doc/appdev.817/a86030/adx16nt5.htm)
* [物理标记语言](http://web.mit.edu/mecheng/pml/standards.htm)


