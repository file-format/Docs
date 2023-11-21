{
"date": "2023-03-07",
  "keywords": [
"注册文件",
"什么是 reg 文件",
"文件",
"reg 文件扩展名",
"扩大"
],
  "author": {
"display_name": "沙基尔·法伊兹"
},
"draft": "false",
"toc": true,
"title": "REG 文件格式 - Windows 注册表文件",
  "description":"了解 REG 格式以及可以创建和打开 REG 文件的 API。",
"linktitle": "REG",
  "menu": {
    "docs": {
      "identifier": "system-reg",
"parent": "system"
}
},
"lastmod": "2023-03-07"
}

## 什么是REG文件？

REG 文件是一种用于导入或导出 Windows 注册表数据的文件格式。 Windows 注册表是一个分层数据库,用于存储 Windows 操作系统和已安装应用程序的配置设置和选项。注册表包含用户首选项,应用程序设置,硬件和软件配置数据等信息。

REG 文件通常具有".reg"文件扩展名,并且是包含一系列特定格式的注册表项和值的纯文本文件。该格式由一个标头部分组成,该标头部分将文件标识为注册表文件,后跟一系列代表注册表项的键和值对。

## REG 文件格式 - 更多信息

以下是 reg 文件格式的示例：

```
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Run]
"Example"="C:\\Example.exe"

[HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced]
"Hidden"=dword:00000001
```

文件的第一行指定注册表编辑器的版本。以下行包含注册表项,其格式为键路径,后跟值名称和值数据。在此示例中,reg 文件包含两个条目：一个将名为"Example.exe"的程序添加到 Windows 启动列表中,另一个将 Windows 资源管理器高级设置中的"隐藏"值设置为"true"。

可以使用文本编辑器（例如记事本）创建和编辑 Reg 文件。它们通常用于备份和恢复目的,以及使用相同的注册表设置配置多台计算机。

## 导入或导出 Windows 注册表

REG 文件是一种用于从 Windows 注册表导入或导出数据的文件类型。 Windows 注册表是一个分层数据库,用于存储 Windows 操作系统和已安装应用程序的配置设置和选项。注册表包含用户首选项,应用程序设置,硬件和软件配置数据等信息。

Reg 文件可用于创建或修改注册表项,它们通常用于备份和恢复目的,以及使用相同的注册表设置配置多台计算机。以下是如何使用 reg 文件向 Windows 注册表添加新的注册表项：

1. 使用文本编辑器（例如记事本）创建一个新的文本文件。
2. 以正确的格式键入注册表项。该格式由一个标头部分组成,该标头部分将文件标识为注册表文件,后跟一系列代表注册表项的键和值对。这是一个例子：

```
Windows Registry Editor Version 5.00

[HKEY_CURRENT_USER\Software\Example]
"Setting1"="Value1"
```

这将在当前用户注册表配置单元的"Software"项下创建一个名为"Example"的新项,并将"Setting1"值设置为"Value1"。

3. 使用 .reg 文件扩展名保存文件。
4. 双击 .reg 文件将新注册表项添加到 Windows 注册表中。

系统将提示您确认是否要将条目添加到注册表中。确认后,新条目将添加到注册表中,您可以使用注册表编辑器工具对其进行验证。

## 参考
* [Windows 注册表](https://en.wikipedia.org/wiki/Windows_Registry)

