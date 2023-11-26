{
"date": "2023-05-31",
  "keywords": [
"桌面文件",
"什么是桌面文件",
"桌面文件包含什么",
"示例桌面文件",
"如何打开桌面文件",
"桌面文件的格式是什么",
"文件",
"桌面文件扩展名",
"扩大"
],
  "author": {
"display_name": "沙基尔·法伊兹"
},
"draft": "false",
"toc": true,
"title": "DESKTOP 文件格式 - 桌面条目文件",
  "description":"了解可以创建和打开 DESKTOP 文件的 DESKTOP 格式和 API。",
"linktitle": "DESKTOP",
  "menu": {
    "docs": {
      "identifier": "settings-desktop",
"parent": "settings"
}
},
"lastmod": "2023-05-31"
}

## 什么是 .DESKTOP 文件？

.desktop 文件是 Linux 桌面环境用来定义应用程序快捷方式和启动器的配置文件。它提供有关应用程序的元数据,例如其名称,图标,执行命令和其他属性。这些文件通常用于在基于 Linux 的系统中的应用程序菜单,桌面启动器或面板中创建快捷方式。

## DESKTOP 文件包含什么？

.desktop 文件遵循特定格式并包含几个关键字段：

- **[桌面条目]：** 这是 .desktop 文件的主要部分标题。
- **名称：** 指定应用程序的名称。
- **评论：** 提供有关应用程序的简短描述或评论。
- **Exec：** 定义启动应用程序时要执行的命令。
- **图标：** 指定与应用程序关联的图标文件的路径。
- **终端：** 指定应用程序是否应在终端窗口中运行。
- **类型：** 指定条目类型,例如"应用程序"或"链接"。
- **类别：** 指定应用程序应在菜单中显示的类别或组。
- **StartupNotify：** 指定桌面环境是否应显示应用程序的启动通知。
- **NoDisplay：** 指定应用程序是否应从菜单中隐藏。
- **操作：** 定义可以在应用程序上执行的附加操作,例如打开特定文件。

## 桌面文件示例

以下是名为"MyTextEditor"的虚构文本编辑器的 .desktop 文件示例：

```
[Desktop Entry]
Name=MyTextEditor
Comment=A simple text editor
Exec=mytexteditor %F
Icon=/path/to/icon.png
Terminal=false
Type=Application
Categories=TextEditor;Utility;
StartupNotify=true
NoDisplay=false
Actions=OpenNewWindow;OpenExistingFile;

[Desktop Action OpenNewWindow]
Name=Open New Window
Exec=mytexteditor

[Desktop Action OpenExistingFile]
Name=Open Existing File
Exec=mytexteditor %U
```

在此示例中,.desktop 文件定义应用程序"MyTextEditor"及其关联属性。它还包括两个附加操作,"打开新窗口"和"打开现有文件",可以从应用程序启动器的上下文菜单访问。

通过将 .desktop 文件放置在特定目录中,例如"/usr/share/applications"或"~/.local/share/applications",桌面环境将识别它并在菜单中相应地显示应用程序或允许从桌面。

## 如何打开 DESKTOP 文件？

有几个软件程序可以打开和处理 .desktop 文件。这些程序通常是基于 Linux 的系统上的文件管理器或桌面环境。这里有些例子：

- **Nautilus（文件）：** GNOME 桌面环境的默认文件管理器。
- **Nemo：** Cinnamon 桌面环境的文件管理器。
- **Dolphin：** KDE Plasma 桌面环境的默认文件管理器。
- **Thunar：** Xfce 桌面环境的默认文件管理器。
- **KDE 菜单编辑器：** 特定于 KDE Plasma 桌面环境的工具,允许您查看和编辑 .desktop 文件。

这些文件管理器和桌面环境提供了用于管理 .desktop 文件的图形界面。它们允许您查看和编辑 .desktop 文件的属性,创建应用程序启动器以及在应用程序菜单或桌面上组织快捷方式。

.desktop 文件是纯文本文件,因此您也可以使用您选择的文本编辑器打开和编辑它们。只需右键单击 .desktop 文件并选择"打开方式"或"使用其他应用程序打开"即可从已安装程序列表中选择文本编辑器。

## DESKTOP 文件的格式是什么？

.desktop 文件格式遵循特定的结构和格式。它是一个纯文本文件,其中包含一组组织成多个部分的键值对。以下是该格式的概述：

- **节标题：** 每个节都以方括号 ([]) 中的标题开头。主要部分通常命名为 [Desktop Entry],其中包含应用程序或启动器的主要元数据。
- **键值对：** 在每个部分中,您可以使用键值对定义属性。格式为"键=值"。键标识属性,值提供相应的数据。
- **属性语法：** 属性值可以是不同类型,包括字符串,布尔值,文件路径或列表。每个属性值的格式取决于其类型。
- **注释：** 您可以使用"#"符号在 .desktop 文件中包含注释。在线"#"后面的任何内容都被视为注释并被忽略。

## 参考
* [桌面条目文件](https://www.baeldung.com/linux/desktop-entry-files)

