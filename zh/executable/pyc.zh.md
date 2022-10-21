{
  "date" : "2022-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 PYC 文件格式和可以创建和打开 PYC 文件的 API。",
  "title" :"PYC 文件格式 - Python 编译文件",
  "linktitle" : "PYC",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-05-09"
}

## 什么是一 .pyc 文件？

PYC 文件是从用 Python 编程语言编写的源代码生成的编译输出文件。当 PY 文件使用 Python 解释器运行时，它被转换为字节码以执行。同时，编译后的字节码也保存为 .pyc 文件，以便以后在适用时从缓存中重用。

## PYC 文件格式的结构

PYC 文件是字节码，它们的文件格式规范不公开。然而，一些消息来源的调查表明，[PYC 文件的结构](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html#:~:text=pyc%20file%20is%20a%20binary,A% 20marshalled%20code%20object.) 包括：

* `一个四字节的幻数`r - 只是随着编组代码的每次更改而更改的两个字节，然后是 0d0a 的两个字节。
* `四字节修改时间戳` - 生成 .pyc 的源文件的 Unix 修改时间戳，以便在源更改时可以重新编译。
* `A marshalled code object` - 代码对象的 marshal.dump 的输出，它是编译源文件的结果。

## 参考

* [.pyc 文件的结构](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html#:~:text=pyc%20file%20is%20a%20binary,A%20marshalled%20code%20object.)

