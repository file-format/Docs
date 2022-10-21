{
  "date" : "2019-10-11",
   "keywords": [ "sln file", "how to run a sln file", "sln", "extension", "format", "What is sln file", "sln file format", "Visual Studio Solution", "Visual Studio solution VS project" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SLN",
  "description":"了解 SLN 文件格式和可以创建和打开 SLN 文件的 API。",
  "linktitle" : "SLN",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是 .sln 文件？
带有 .SLN 扩展名的文件代表 **Visual Studio 解决方案** 文件，该文件将有关项目组织的信息保存在解决方案文件中。这种解决方案文件的内容以纯文本形式写入文件内，可以通过在任何文本编辑器中打开文件来观察/编辑。解决方案文件中包含的信息保持不变，并用于加载与解决方案相关的信息，例如 [projects ](/zh/programming/csproj/) 和任何其他所需信息。解决方案文件引用的项目文件包含附加信息，以使环境能够使用该项目的项填充层次结构。 .sln 文件中不存储任何数据，但如果需要，可以将项目信息写入 .sln 文件。

## **SLN 版本历史** ##

随着时间的推移，解决方案格式版本随着每个 Microsoft Visual Studio 解决方案的发展而演变。有关这些的详细信息如下。


|Visual Studio 版本|解决方案格式版本
---|---|
|2003|8.00
|2005|9.00
|2008|10.00
|2010|11.00
|2013|12.00
|2015|12.00
|2017|12.00

### **解决方案文件的内容** ###

解决方案文件由环境读取以加载项目的几个部分组成。示例 .sln 文件内容如下所示。

```
Project("{F184B08F-C81C-45F6-A57F-5ABD9991F28F}") # "Project1", "Project1.vbproj", "{8CDD8387-B905-44A8-B5D5-07BB50E05BEA}"  
EndProject  
Global  
  GlobalSection(SolutionNotes) # postSolution  
  EndGlobalSection  
  GlobalSection(SolutionConfiguration) # preSolution  
       ConfigName.0 # Debug  
       ConfigName.1 # Release  
  EndGlobalSection  
  GlobalSection(ProjectDependencies) # postSolution  
  EndGlobalSection  
  GlobalSection(ProjectConfiguration) # postSolution  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.ActiveCfg # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.Build.0 # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.ActiveCfg # Release|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.Build.0 # Release|x86  
  EndGlobalSection  
  GlobalSection(ExtensibilityGlobals) # postSolution  
  EndGlobalSection  
  GlobalSection(ExtensibilityAddIns) # postSolution  
  EndGlobalSection  
EndGlobal
```

### **项目声明** ###

一个解决方案文件可以包含多个项目声明以及不同项目类型的声明。例如，单个解决方案文件可以包含 CSharp 以及 VB.NET 项目。这些类型在使用 [Project-Type-GUID](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs) 的解决方案中进行区分。上面的项目声明可以概括如下，以便于理解。

```
Project("{Project-Type-GUID}") # "Project-Name", "Project-Path.extension", "{Project-GUID}"
```

`Project-Type-GUID:` Project-Type-GUID 对于不同的项目类型是唯一的，解决方案阅读器使用它来识别项目的类型。在这种情况下，F184B08F-C81C-45F6-A57F-5ABD9991F28F 表明它是一个 VB.NET 项目。

`项目 GUID：` 项目的唯一 GUID，将其与解决方案中的其他项目区分开来。解决方案中项目的唯一 ID 使解决方案中的其他项目可以访问它。

根据 .sln 文件的项目部分中包含的信息，环境会加载每个项目文件。然后，项目本身负责填充项目层次结构并加载任何嵌套项目。对解决方案所做的任何更改都会在保存或关闭项目时保存回解决方案文件。

## Visual Studio 解决方案 VS 项目

**项目：** 从逻辑上讲，当您开始使用 Visual Studio 创建应用或软件时，您将启动一个新项目。一个项目包含所有必要的文件，例如源代码、图标、图像、数据文件等，这些文件将被编译成可执行的应用程序、网站或库。

**解决方案：** 一个解决方案包含一个或多个项目。因此，该解决方案就像 Visual Studio 项目的容器。从逻辑上讲，我们可以说有人想为他的业务获得一个完整的解决方案，包括网站、桌面应用程序、restful 服务和移动应用程序。

＃＃＃ **参考** ＃＃＃

* [解决方案文件 - 由 MSDN 提供](https://docs.microsoft.com/en-us/visualstudio/extensibility/internals/solution-dot-sln-file?view#vs-2017)
* [项目类型 GUID](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs)

