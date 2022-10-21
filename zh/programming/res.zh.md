{
  "date" : "2021-04-23",
  "keywords": [ "RES File", "how to open a res file", "what is a res file", "extension", "format", "RES file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RES - C++ 编译资源脚本",
  "description":"通过 RES 示例和可创建和打开 RES 文件的 API 了解 RES 文件格式。",
  "linktitle" : "RES",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## 什么是一 .res 文件？
带有 .res 后缀或扩展名的文件可以属于许多文件格式类别。这里我们讨论的是 RES 文件格式，它是一个 C++ 编译资源脚本；由 Microsoft 资源编译器 (rc) 创建的包含资源数据的二进制文件；基于资源定义文件的内容；与其父软件项目相关。 .res 文件通常重新格式化为资源对象文件，以将其链接到应用程序的可执行文件。

## RES 文件格式
RES 文件格式属于 Microsoft 资源编译器 (rc)。资源编译器是一种工具，用于编译应用程序使用的光标、图标、菜单和对话框等资源。资源文件通常具有 .res 扩展名；包含资源，例如光标、图像和版本信息。 RES 文件可以是 16 位或 32 位资源文件。
## 资源文件结构
一个资源文件包含一系列不同的资源条目。每个条目都包含一个资源标题和相关数据。资源头通常在文件中以 DWORD 对齐，并包含以下内容：

- 一个 **DWORD** 指定资源头的大小
- 一个**DWORD**来指定资源数据的大小
- 资源类型
- 资源名称
- 其他资源信息

资源头结构定义了 RES 文件的格式。资源的数据跟在资源头之后。一些资源还添加了特定于资源的组标头模式，以提供有关一组资源的信息。以下是一些资源条目类型及其描述：

### 加速器表资源
加速表是 RES 文件中没有组头的资源条目。 **ACCELTABLEENTRY** 模式定义了快捷键表中的每个条目。一个 RES 文件可能有多个加速器表。

### 光标和图标资源
虽然，系统将每个图标和光标视为一个单独的文件，但这些都是作为一组图标资源或一组光标资源存储在 RES 文件中的。图标和光标资源的文件格式相同。资源组标题跟在 .res 文件中的所有单个图标或光标组组件之后。

### 对话框资源
对话框也被实现为 RES 文件中的资源条目。它包含一个 **DLGTEMPLATE** 对话框标题模式和一个用于对话框中每个特定控件的 **DLGITEMTEMPLATE** 模式。 **DLGTEMPLATEEX** 和 **DLGITEMTEMPLATEEX** 模式解释了扩展对话框资源的格式。

### 字体资源
一个菜单资源包含一个 **MENUHEADER** 模式，随后包含一个或多个 **NORMALMENUITEM** 或 **POPUPMENUITEM** 模式，一个用于菜单模板中的每个菜单项。 **MENUEX_TEMPLATE_HEADER** 和 **MENUEX_TEMPLATE_ITEM** 模式解释了扩展菜单资源的格式。

### 消息表资源
消息表由格式化文本组成，用于显示为错误消息或在消息框中。消息表资源中的主要模式是 **MESSAGE_RESOURCE_DATA** 结构。

### 版本资源
版本资源中的主要模式是 **VS_FIXEDFILEINFO**。其他模式包括用于存储语言信息相关数据的 **VarFileInfo** 和用于自定义字符串信息的 **StringFileInfo**。




## 参考

* [资源文件格式](https://docs.microsoft.com/en-us/windows/win32/menurc/resource-file-formats)
 


 



