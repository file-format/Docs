{
  "date" : "2023-01-31",
  "keywords" :["运行文件","什么是运行文件","文件","如何打开运行文件","运行文件扩展名","扩展名"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 RUN 文件格式以及可以创建和打开 RUN 文件的 API。",
  "title" :"RUN 文件格式 - Linux 可执行文件",
  "linktitle" : "RUN",
  "menu" : {
    "docs" : {
      "identifier":"executable-run",
      "parent" : "executable"
}
},
  "lastmod" : "2023-01-31"
}

## 什么是 .RUN 文件？

.run 文件格式通常用于在 Linux 环境中分发软件或应用程序安装程序。要安装该软件，您需要使该文件可执行，可以使用以下命令来完成：

```bash
chmod +x file_name.run 
```

然后，您可以使用以下命令运行该文件：

```bash
./file_name.run 
```

安装过程可能会有所不同，具体取决于您尝试安装的特定文件和程序。

.run 文件格式是一种 shell 脚本，用于在 Linux 环境中分发软件或应用程序安装程序。它是一个独立的软件包，包含安装软件所需的所有内容，包括二进制文件、库和配置文件。

请务必注意，.run 文件也可能包含恶意代码，因此在运行文件之前验证文件来源并扫描病毒始终是一个好主意。

此外，某些 .run 文件可能需要 root 权限才能运行和安装，因此您可能需要使用“sudo”命令以提升的权限运行该文件：

```bash
sudo ./filename.run
```

## 如何打开 RUN 文件？

要打开 .run 文件，您需要使其可执行，这可以使用“chmod”命令来完成：

```bash
chmod +x filename.run 
```

文件可执行后，您可以通过键入以下命令来运行它：

```bash
./filename.run
```

运行 .run 文件与在文本编辑器中打开它不同。运行 .run 文件将执行其指令，这些指令可以是从安装程序到运行脚本的任何内容。要查看 .run 文件的内容，您需要在文本编辑器（例如 nano 或 vim）中打开它：

```
nano filename.run
```
或者
```
vim filename.run
```

## 参考
* [如何在 Ubuntu 中执行 .bin 和 .run 文件](https://vitux.com/how-to-execute-bin-and-run-files-in-ubuntu/)


