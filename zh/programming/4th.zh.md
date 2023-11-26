
{
  "date" : "2023-02-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"第四个文件 - 第四种语言文件格式",
  "description":"通过示例和可以创建和打开 4th 文件的 API 了解什么是 .4th 文件格式。",
  "linktitle" : "4th",
  "menu" : {
    "docs" : {
      "identifier":"programming-4th",
      "parent" : "programming"
}
},
  "lastmod" : "2023-02-09"
}

## 什么是第四个文件？

具有 .4th 文件扩展名的文件是为 **Forth 编程语言** 创建的编程文件。它包含用 Forth 编程语言编写的程序的源代码，并在执行程序时生成输出。它只是类似于 [C](/zh/programming/c/) 和 [C++](/zh/programming/cpp/) 源文件的另一种编程语言文件。

## 第四种文件格式 - 更多信息


### 第四种编程语言代码示例

下面是一个用 Forth 编写的简单程序示例，用于计算给定数字的阶乘：

```
: factorial ( n -- n! )
   dup 0=
   if
      drop 1
      exit
   then
   1
   swap
   begin
      dup 1-
      dup 0=
      if
         drop
         exit
      then
      swap
      *
   repeat
;

```

在此示例中，阶乘词采用单个参数 n 并返回其阶乘。 dup 字复制堆栈顶部的值，drop 丢弃堆栈顶部的值，* 将堆栈顶部的两个值相乘。 if 和 begin/until 结构控制程序的流程。

要使用该程序，您需要将定义输入 Forth 解释器，然后使用您想要查找阶乘的数字调用阶乘词：

```
10 factorial .
```
这将导致输出 3628800，它是 10 的阶乘。

## 参考

* [Forth 编程语言](https://en.wikipedia.org/wiki/Forth_(programming_language))

