{
  "date" : "2021-07-15",
  "keywords" :["LNK","扩展名","文件","格式","系统","LNK 文件","链接","LNK 文件","LNK 文档","应用程序","程序"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LNK - 链接文件格式",
  "description":"了解 LNK 文件格式和可以创建和打开 LNK 文件的 API。",
  "linktitle" : "LNK",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-15"
}

## 什么是一 .lnk 文件？ ##

LNK 文件，类似于 Mac 系统上的标识，是 Windows 替代品或“链接"，用作与原始图像文档文件夹或程序的连接。它包含快捷方式目标的类型、位置和文件名，以及打开目标文档的应用程序和附加的快捷键。

在 Windows 中，直接创建文件、文件夹或可执行程序，然后选择创建快捷方式。文件格式的位置和“Beginning"目录是 LNK 文件的两个基本特征。 LNK 文件的文件格式被屏蔽，弯曲的箭头表示它们是快捷方式。

## LNK 文件格式##

LNK 文件格式通常具有与其目标文件相同的图标，但添加了一个小卷曲箭头以表明文件指向不同的位置。双击快捷方式时，它的行为就像用户双击了实际文件一样。

包含应用程序快捷方式的 LNK 文件可能具有影响程序运行方式的属性。要更改属性，请右键单击快捷方式文件并选择 **Properties**，然后更改 Target 字段。

LNK 文件不是文件扩展名，而是 Windows 资源管理器扩展名。作为终端扩展，.lnk 文档只能在 Windows 资源管理器中用于替换文件，它们在 Windows 资源管理器中除了用作本地文档的快捷方式外，还有其他用途。这些文件也以字母“L"开头。

虽然快捷方式在创建时会链接到特定文件和目录，但如果将目标更改为其他位置，它们可能会变得无法操作。资源管理器将开始修复打开时指向死目标的快捷方式文件夹。


## 技术规格##

仅当未选中“隐藏已识别文件类型的扩展名"文件夹查看设置时，Windows 才不会显示文档快捷方式的 .lnk 文档扩展名。虽然不建议这样做，但您可以通过从 HKEY_CLASSES_ROOT\lnk 文件 Windows 注册表项中删除“NeverShowExt"属性来启用文件扩展名。

为此，请执行以下步骤：

*通过在任务栏搜索字段中输入“Regedit"并选择程序来打开“注册编辑器"
* 在应用程序中，导航到 Computer\HKEY HKEY_CLASSES_ROOT\lnkfile 位置
* 通过右键单击该项目并选择“导出"来备份该项目
* 选择并删除“NeverShowExt"属性
* 应重新启动 Windows


## 参考 ＃＃

* [LNK - Wikipedia](https://en.m.wikipedia.org/wiki/Shortcut_(computing))
