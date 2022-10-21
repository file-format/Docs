{
  "date" : "2022-04-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 AHK 文件格式和可以创建和打开 AHK 文件的 API。",
  "title" :"AHK 文件格式- AutoHotkey 脚本文件",
  "linktitle" : "AHK",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-04-25"
}

## 什么是一 .ahk 文件？

AHK 文件是使用 AutoHotkey 软件应用程序生成的脚本文件，用于在 Microsoft Windows 中自动执行任务。它包含使用可用于执行即时操作的快捷键自动执行任务的说明。该文件由 AutoHotkey 执行，所有操作都按顺序执行。 AHK 文件功能强大，可以使用热键定义的热键执行复杂的任务。 AHK 文件可以使用 Microsoft Notepad 和 Notepad++ 等文本编辑器打开。

## AHK 文件格式

AHK 文件以纯文本文件的形式保存到光盘中，并包含可由 AutoHotkey 执行的代码行。 AutoHotkey 是一种免费的开源脚本语言，允许用户创建从简单到复杂的脚本来执行诸如表单填充、自动单击、执行宏等操作。AHK 文件至少可以执行单个操作然后退出.

有一些工具可用于将 AHK 转换为 [Exe](/zh/executable/exe/) 文件。

### AHK 示例

下面的示例使用 Win+Z 键运行 Microsoft 记事本，如果它已经在运行，则将其置于最前面。

```
#z::Run https://www.autohotkey.com  ; Win+Z

^!n::  ; Ctrl+Alt+N
if WinExist("Untitled - Notepad")
    WinActivate
else
    Run Notepad
return
```

## 如何创建 AHK 文件？

以下步骤可用于创建 AHK 文件。这些假设 AutoHotkey 已经安装在机器上。

* 右键单击您的桌面。
* 在菜单中找到“新建"。
* 单击“新建"菜单中的“AutoHotkey 脚本"。
* 给脚本一个新名字。
* 在桌面上找到新创建的文件并右键单击它。
* 点击“编辑脚本"。
* 应该会弹出一个窗口，可能是记事本。
* 保存文件。

## 参考

* [AutoHotkey](https://www.autohotkey.com/)
* [批处理文件 - 维基百科](https://en.wikipedia.org/wiki/Batch_file)

