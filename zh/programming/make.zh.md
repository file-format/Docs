{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"制作文件 - Xcode Makefile 脚本文件",
  "description":"了解 XCode MakeFile 格式和可以创建和打开 MakeFile 文件的 API。",
  "linktitle" : "MAKE",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}


## 什么是 .make 文件？

MAKE 文件是组织代码编译的 XCode 脚本文件。它用于从多个源代码文件编译和链接程序。这有助于决定在需要更新应用程序时需要重新编译大型应用程序的哪些部分。 Make files 使用一系列指令来运行，具体取决于哪些文件已更改。

## MAKE 文件格式示例

使用 Make 实用程序执行以下内容，输出如下。

```
hello:
	echo "hello world"
```
**制作输出**

```
$ make
echo "hello world"
hello world
```

## 参考
* [XCode 和 Make - Apple 论坛](https://developer.apple.com/forums/thread/657458)
* [Object-C 指南](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

