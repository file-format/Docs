{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AWK 文件格式 - AWK 脚本文件",
  "description":"了解 AWK 文件格式和可以创建和打开 AWK 文件的 API。",
  "linktitle" : "AWK",
  "menu" : {
    "docs" : {
      "identifier" : "programming-awk",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## 什么是一 .awk 文件？

AWK 文件是为文本处理应用程序 **AWK** 创建的脚本文件，它与 Unix 和 Linux 操作系统捆绑在一起。它包含对文本或文件内容执行操作的逻辑指令，例如匹配、替换和打印文本。这有助于从输入文件生成报告和格式化文本。在大多数 linux/unix 发行版上，awk 实用程序通常位于 /usr/bin/awk 中。

## 如何创建 AWK 脚本？

可以在 Linux/Unix 操作系统上的任何文本编辑器中创建或打开 AWK 文件。可以创建一个新的 AWK 脚本文件，如下所示。

```
$ vi script.awk
```

这将在文本编辑器中打开 AWK 文件。在文本编辑器中输入一些语句，如下所示。

```
#!/usr/bin/awk -f
BEGIN { printf "%s\n","Writing my first Awk executable script!" }
```
该文本内容的第一行解释如下。

* \#! – 称为“Shebang"，它为脚本中的指令指定解释器
* /usr/bin/awk – 是解释器
* -f – 解释器选项，用于读取程序文件

## 如何执行 AWK 脚本？

保存文件并通过发出以下命令使脚本可执行：
```
$ chmod +x script.awk
```

然后可以按如下方式运行该脚本。

```
$ ./script.awk
```

这导致以下输出。

```
Writing my first Awk executable script!
```

## 参考 ＃＃

* [使用 awk 编程语言编写脚本](https://www.tecmint.com/write-shell-scripts-in-awk-programming/)

