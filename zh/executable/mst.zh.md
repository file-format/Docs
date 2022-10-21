{
  "date" : "2021-06-30",
  "keywords" :["mst 文件","mst 文件格式","什么是 mst 文件","文件","mst 示例","mst 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 MST 文件格式和可以创建和打开 MST 文件的 API。",
  "title" :"MST - Windows 安装程序包文件",
  "linktitle" : "MST",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## 什么是一 .mst 文件？
扩展名为 .mst 的文件用于转换 MSI 包的内容。系统管理员通常使用它们将自定义设置应用于现有的 MSI 文件。 MST 文件在其软件分发系统（例如组策略）中与原始 MSI 包一起使用。 MST 文件通常用于软件开发和测试，以配置其开发中的软件版本。

## MST 文件格式
MST 或转换文件用于收集文件中使用 Microsoft Windows 安装程序的程序的安装选项。这些文件通常用于安装程序 (MSIEXEC.EXE) 命令行，或用于软件安装的组策略；在 Microsoft Active Directory 域中。 MST 文件也可以与打包的可执行安装程序一起使用。一般情况是有人想将命令行参数传递给打包的安装程序。为此，您需要一个将 WRAPPED_ARGUMENTS 属性添加到属性表的 MST 文件。无法使用通用编辑器创建或编辑这些文件。为此可使用特定工具。

### 如何使用 MST 文件？
MST 文件可以使用各种工具生成，通常使用 Ocra 来生成 MST 文件。然后可以根据需要自定义设置并将它们保存在特定位置。之后，可以将 MST 文件与 MSI 文件结合使用。如果你想测试这个文件；在命令行上使用以下语法

```
msiexec /i setup_1.0.msi TRANSFORMS=mylog.mst
```
### TRANSFORMS 属性

您还可以使用 Windows 安装程序的 **TRANSFORMS** 属性，它实际上是安装程序在安装软件包时应用的转换列表。安装程序按照 TRANSFORM 属性中列出的顺序执行转换。可以通过带有 .mst 扩展名或完整路径的文件名指定转换。要指定多个转换，请分隔每个文件名或分号，如下例所示。

```
TRANSFORMS=transform1.mst;transform2.mst;transform3.mst
```

## 参考

* [MST 转换文件](https://www.exemsi.com/documentation/mst-transformation-files/)
* [转换属性](https://docs.microsoft.com/en-us/windows/win32/msi/transforms)


