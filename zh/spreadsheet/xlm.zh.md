{
  "date" : "2019-12-10",
  "keywords" :["XLM","文件","扩展名","文件格式","Microsoft Excel 宏文件","电子表格"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"您的文件格式指南,了解什么是 XLM 宏文件以及可以创建和打开 XLM 文件的 API。",
  "title" :"什么是 XLM 文件？",
  "linktitle" : "XLM",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## 什么是一 .xlm 文件？

XLM，即 Excel 宏，是一种用于存储宏的电子表格文件。从应用程序的角度来看，宏是一组用于自动化流程的指令。宏用于记录对 [XLS](/zh/spreadsheet/xls/) 文件格式重复执行的步骤，并通过再次运行宏来促进执行操作。使用 Visual Basic 编辑器从 Excel 工作簿中使用 Microsoft 的 Visual Basic for Applications (VBA) 对宏进行编程，并且可以直接从那里运行/调试。

## 历史简介 ＃＃

Microsoft Excel 自首次公开发布以来就支持宏编程。宏的功能在后续版本的 Excel 中保持不变，并根据新功能进行了扩展。 XLM 是 Excel 4.0 至 Excel 的默认宏语言。 Excel 5.0 默认在 VBA 中录制宏，但在 5.0 版本中仍允许 XLM 录制作为选项。在 5.0 版之后，该选项已停用。所有版本的 Excel，包括 Excel 2010 都能够运行 XLM 宏，但 Microsoft 不鼓励使用它们。

## 在 XLM 中录制宏##

Excel 提供了易于使用的录制宏的步骤。它需要您安装开发者工具才能使用宏。宏录制完成后，它会记录每个用户操作，以便稍后播放。宏录制实际上涉及用户在录制开始后执行的所有步骤。因此，如果您在宏录制开始后将单元格的内容设置为粗体、斜体并设置其文本对齐方式，则所有这些命令都将被录制。每个录制的宏都可以分配一个快捷方式，以便以后快速播放。宏录制以可以使用 Visual Basic 编辑器 (VBE) 编辑的宏的形式生成 VBA 代码。

## Excel 对象模型##

为此，宏使用 VBA 例程并遵循 [Excel 对象模型](https://docs.microsoft.com/en-us/office/vba/api/overview/excel/object-model)。该模型通过用户定义的命令工具栏、命令栏或消息框识别电子表格的对象以与电子表格交互。例如，使用 Workbook 对象授予对工作簿属性的访问权限。同样，模型中有 Worksheet 对象以编程方式处理工作簿的工作表。

## 宏和安全##

VBA 允许访问应用程序的所有领域以及文件系统，并且也可能是危险的。当与可以在他最后运行文件的人共享工作簿时，这会引起关注。那是 Microsoft Excel 警告打开这样的文件。可以使用数字签名对宏进行认证，以便其他用户验证这些是值得信赖的。因此，可以在验证其来源后启用宏。

## 参考 ＃＃

* [[MS-XLS] - Excel 二进制文件格式结构](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)
* [宏编程](https://en.wikipedia.org/wiki/Microsoft_Excel#Macro_programming)

