{
  "date" : "2023-08-07",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Shell 脚本 - 如何在 Ubuntu 和 Linux 上运行它",
  "description":"了解什么是 Shell 脚本以及如何在 Ubuntu 和 Linux 上运行它",
  "linktitle" : "SHELL SCRIPT",
  "menu" : {
    "docs" : {
      "identifier": "misc-shell-script-zh",
      "parent" : "misc"
}
},
  "lastmod" : "2023-08-07"
}

## 什么是 Shell 脚本？

Shell 脚本涉及在纯文本文件中编写一系列命令，通常称为 **Shell 脚本**。这些脚本由 shell（命令行解释器）执行。最常见的 shell 包括

1. Bash (Bourne Again SHell)
2. Zsh（Z 外壳）
3. 鱼。

Shell 脚本的范围可以从简单的单行代码到复杂的程序，它们用于执行各种任务，例如文件操作、系统管理和重复任务的自动化。

## Shell 脚本的优点：

1.  **自动化：** Shell 脚本允许用户自动执行重复性任务，从而节省时间并减少人为错误的机会。
    
2.  **定制：** 用户可以创建适合其特定需求的脚本，提供高度的定制。
    
3.  **批处理：** Shell 脚本非常适合处理批处理任务，其中多个命令需要按顺序执行。
    
4.  **系统管理：** Shell 脚本通常用于系统管理任务，例如备份、日志轮换和软件安装。

## 编写一个简单的 Shell 脚本：

让我们创建一个打印问候消息的基本 shell 脚本。打开文本编辑器并创建一个名为greeting.sh”的文件。添加以下行：

```
#!/bin/bash
# This is a simple shell script

echo "Hello, welcome to the world of shell scripting!"
```

保存文件并通过在终端中运行以下命令使其可执行：

```
chmod +x greeting.sh
```

现在，您可以执行该脚本：

```
./greeting.sh
```

输出应该是：

```
Hello, welcome to the world of shell scripting!
```

## 在 Ubuntu 和 Linux 上运行 Shell 脚本：

现在，我们将讨论**如何在 Ubuntu 和 Linux 中运行 .sh 文件**。

1.  **使脚本可执行：** 在运行 shell 脚本之前，请确保它是可执行的。使用前面所示的chmod”命令。
    
2.  **导航到脚本目录：** 打开终端并使用 `cd` 命令导航到包含 shell 脚本的目录。
    
3.  **运行脚本：** 通过在终端中键入 `./scriptname.sh` 来执行脚本，将scriptname”替换为脚本的实际名称。
    
```
cd path/to/script
./greeting.sh
``` 

4.  **使用 Bash 命令：** 如果您的脚本以 `#!/bin/bash` 开头（称为 **shebang**），您也可以使用 `bash` 命令运行它。

```
bash greeting.sh
```

## Shell脚本中的$@是什么意思？

在 shell 脚本中，`$@` 代表传递给脚本的所有命令行参数。它通常用于将参数列表作为单独的实体进行引用。当在双引号中使用时，例如$@”，它会保留单个参数，并考虑空格和特殊字符。

以下是简要说明：

- `$@`：表示传递给脚本或函数的所有位置参数（参数）。每个参数都被视为单独的单词。
    
- `$@`：当用双引号引起来时，保留参数的分隔，允许在各个参数中使用空格或特殊字符。
    

这是一个简单的例子来说明：

```
#!/bin/bash

# Save this script as example.sh

echo "The total number of arguments is: $#"
echo "The arguments are: $@"
echo "The arguments with double quotes are: \"$@\""
```

当您使用参数运行此脚本时，例如：

```
bash example.sh arg1 "argument 2" arg3
```

它将输出：

```
The total number of arguments is: 3
The arguments are: arg1 argument 2 arg3
The arguments with double quotes are: "arg1" "argument 2" "arg3"
```

正如您所看到的，`$@` 代表所有参数，而 `$@` 保留各个参数，即使它们包含空格。

