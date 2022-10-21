{
  "date" : "2019-10-11",
  "keywords" :[ "vbproj", "file", "extension", "file format", "VB Project File", "Programming Guide"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBPROJ",
  "description":"了解 VBPROJ 文件格式和可以创建和打开 VBPROJ 文件的 API。",
  "linktitle" : "VBPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## 什么是一 .VBPROJ 文件？

带有 .vbproj 扩展名的文件是 Microsoft Visual Basic 项目文件，Microsoft 的 MSBuild 引擎使用该文件在 Visual Studio 解决方案中构建项目。它类似于用 [C#](/zh/programming/cs/) 编写的 .NET 项目的 [CSPROJ](/zh/programming/csproj/) 文件。 MSBuild 引擎从 VBPROJ 文件中读取不同组中包含的信息并生成输出文件。 VBPROJ 文件可以包含与定义项目的全局标识符、类和属性相关的信息。 VBPROJ 文件可以使用 Microsoft Visual Studio 和任何常见的文本编辑器（如 Windows 和 MacOS 操作系统上的记事本）打开和编辑。

## VBPROJ 文件格式 - 更多信息

VBPROJ 文件是基于 [MSBuild XML 架构](https://docs.microsoft.com/en-us/visualstudio/msbuild/msbuild-) 以 [XML](/zh/web/xml/) 文件格式编写的文本文件项目文件架构参考？view=vs-2019）。 VBPROJ 文件包含 XML 标记形式的信息，这些标记定义与该特定设置组相关的信息。强烈建议在 Microsoft Visual Studio IDE 中打开和编辑这些设置文件。

### VBPROJ 元素

VB 设置文件的组成元素如下图所示。

{{< figure src="../vbproj.png" alt="VBPROJ 文件格式" >}}

下表简要说明了这些元素。

|元素|描述|
---|---|
|项目|每个项目文件的根元素，除了标识项目文件的 XML 模式之外，还可以包含指定构建过程入口点的属性|
|属性和条件|属性由键值对组成，并在 PropertyGroup 元素中定义。属性元素名称代表属性键，元素内容定义属性值。|
|项目和项目组|项目文件中的项目是构建过程的输入，例如文件代码文件、配置文件、命令文件和构建过程所需的其他文件。项目是并且必须在 ItemGroup 元素中定义。|
|目标与任务| Task 元素代表一个单独的构建指令（或任务）。 MSBuild 包含大量预定义任务，例如 Copy、CSC、VBC、Exec。任务必须始终包含在 `Target` 元素中，该元素是一组按顺序执行的一个或多个任务，一个项目文件可以包含多个目标。

## 参考

* [了解项目文件](https://docs.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file)
* [MSBuild 架构元素](https://docs.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019)

