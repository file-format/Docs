{
  "date" : "2019-10-11",
  "keywords": [ "sh file", ".sh file", "extension", "format", "sh file example", "sh file format", "how to run sh file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SH - Bash Shell 脚本文件",
  "description":"了解 SH 文件格式和可以创建和打开 SH 文件的 API。",
  "linktitle" : "SH",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-21"
}

## 什么是一 .sh 文件？

扩展名为 .sh 的文件是脚本语言命令文件，其中包含要由 Unix shell 运行的计算机程序。它可以包含一系列顺序运行的命令，以执行诸如文件处理、程序执行和其他此类任务之类的操作。这些由用户或批量从命令行界面执行，以同时执行多个操作。脚本文件可以在文本编辑器中打开，例如 Notepad、Notepad++、Vim、Apple Terminal 和 Windows、MacOS 和 Linux OS 上的其他类似应用程序。

## SH 文件格式

SH 文件按照定义的语法以纯文本形式编写。这些脚本文件支持：

* `Comments` - 注释以 # 开头，并被 shell 忽略。
* `Shortcuts` - 这些可用于重命名命令以实现简短且易于执行。
* `Batch Jobs` - 几个命令可以自动执行，否则需要手动输入。这消除了等待用户触发序列的每个阶段的需要。
* `Generalization` - 使用简单的循环，可以实现更多的泛化操作，例如从一个图像到另一个图像的转换。

## SH 文件示例

```
$ echo '#!/bin/sh' > my-script.sh
$ echo 'echo Hello World' >> my-script.sh
$ cat my-script.sh
#!/bin/sh
echo Hello World
$ chmod 755 my-script.sh
$ ./my-script.sh
Hello World
```
## 如何运行 SH 文件？
SH 文件通常在 Linux 上运行，即使在 Windows 中，您也需要使用 Putty 等软件连接 Linux 终端来运行 sh 文件。以下是在 Linux 终端上运行 SH 文件的步骤。

1、打开Linux终端，进入SH文件所在目录。
2. 通过使用 `chmod` 命令，设置脚本的执行权限（如果尚未设置）。
3. 使用以下方法之一运行脚本
1.`./filename.sh`
2.`sh 文件名.sh`
3. `bash script-name-here.sh`

## 参考

* [Bashscripting 初学者](https://help.ubuntu.com/community/Beginners/BashScripting)
* [Shellscript](https://www.shellscript.sh/)

