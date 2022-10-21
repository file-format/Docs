{
  "date" : "2021-06-30",
  "keywords" :["msi 文件","MSI 文件格式","什么是 msi 文件","文件","msi 示例","msi 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 MSI 文件格式和可以创建和打开 MSI 文件的 API。",
  "title" :"MSI - Windows 安装程序包文件",
  "linktitle" : "MSI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## 什么是一 .MSI 文件？
用于安装和启动 Windows 程序的 MSI 文件； Microsoft Windows 的完整软件包，其中包含典型软件程序的安装信息，包括要安装的基本文件和有关安装位置的信息。 MSI 文件还可能包含软件更新包。 MSI 文件类似于 [EXE](/zh/executable/exe/)，但 EXE 有时可能不包含安装程序信息，执行 EXE 文件时可能会直接运行软件程序。

## MSI 文件格式
Windows Installer 实际上是 Microsoft Windows 的 API（应用程序编程接口）和软件组件，用于安装,删除和维护软件程序。安装信息和可选文件被打包为安装包和结构为 COM 结构化存储的松散关系数据库；众所周知的 **MSI 文件**，具有 .msi 文件扩展名。具有文件扩展名**.mst** 的包包含Windows Installer 的**Transformation Scripts**，具有**.msm** 扩展名的文件包含**Merge Modules** 和文件扩展名**.pcp**用于**补丁创建属性**。 Windows Installer 在对其早期版本 Setup API 进行了重大更改后变得更加先进。 GUI 框架和自动生成卸载顺序是 Windows Installer 的新功能。它现在已被视为独立可执行安装程序框架的替代方案。

### MSI 包的逻辑结构
包指定安装一个或多个完整产品，通常由**GUID** 标识。产品由一个或多个组件组成，并分为各种功能。 Windows Installer 不会同时处理各种产品之间的依赖关系。包的逻辑结构由以下元素组成：

- **产品**：一个单独的、已安装的、工作的程序或组合在一起的多个程序的集合是一个产品。产品由唯一的 GUID 标识。
- **功能**：可能包含任意数量的组件和其他子功能。较小的软件包可以包含单个功能。
- **Components**：Windows Installer 将组件视为一个单元；可以包含程序文件、文件夹、注册表项、COM 组件和快捷方式。
- **密钥路径**：密钥路径是包作者指定为对给定组件至关重要的特定文件、ODBC 数据源或注册表项。

## 参考

* [Windows 安装程序 - 维基百科提供](https://en.wikipedia.org/wiki/Windows_Installer)


