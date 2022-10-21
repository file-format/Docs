{
  "date" : "2021-05-25",
  "keywords" :[ "DML","DML 文件", "DML 文件格式", "DML 文件类型", "文件", "类型", "什么是 DML 文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DML - DynaScript HTML 文件",
  "description":"了解 DML 文件格式和可以创建和打开 DML 文件的 API。",
  "linktitle" : "DML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-25"
}

## 什么是一 .dml 文件？

扩展名为 .dml 的文件是使用 DyanScript 创建的网页脚本页面代码文件。 DynaScript 是一种动态的 [HTML](/zh/web/html/) 脚本语言，它与 ECMAScript 兼容，并提供与其他脚本语言相同的大部分功能。它类似于 ColdFusion 代码和 Microsoft Active Server Pages (ASP) 代码。 DML 文件可以在与其他 HTML 页面类似的标准 Web 浏览器中打开和查看。

## DML 文件格式

DML 文件以纯文本文件格式创建，可以使用文本编辑器打开以查看代码。使用 DML 脚本语言编写代码可用于在服务器端托管的 DML 页面上动态生成 HTML。 DynaScript 由以下语言元素构建：


* SCRIPT 标签 - 这些作为 HTML 注释嵌入到文档中。 HTML 注释由 \ 标记<!-- tag.
* 文字 - 这些是 DynaScript 文件中的固定值。这些示例包括整数，如 s 123 、 0x3F 、 0123，浮点数，如 456.789 、 3.2e-8，布尔值，如 true 或 false，以及字符串，如“西班牙的雨"
* 变量 - DynaScript 变量无需定义或分配给固定数据类型。在表达式中使用变量之前，它必须有一个值；否则会生成运行时警告。
* 表达式 - 这些是变量、文字值、运算符和其他表达式的组合。赋值语句的右侧是表达式。
* 运算符 - 这些运算符对一个或多个称为操作数的表达式进行操作。它们可以是三元、二元或一元：三元运算符作用于三个表达式，二元运算符作用于两个表达式，而一元运算符作用于一个。
* 语句 - 这些控制脚本流程、操作对象和一般编程。通常，这些语句遵循标准的 C 和 Java 语法。示例是 if-else、do-while 循环、switch、break、continue 等，就像任何其他脚本语言一样。
* 函数 - 函数与任何其他脚本语言一样，允许您在文档中将一组指令封装为函数一次，然后在整个文档中多次使用它（通过调用函数）。 DynaScript 还支持函数。
* 对象 - DynaScript 是面向对象的，支持“对象"以及封装、多态和继承等面向对象的基本概念。

