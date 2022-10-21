{
  "date" : "2019-10-11",
  "keywords": [ "csproj file", "csproj", "extension", "format", "What is a csproj file", "csproj file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSPROJ",
  "description":"了解 CSPROJ 文件格式和可以创建和打开 CSPROJ 文件的 API。",
  "linktitle" : "CSPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-21"
}

## 什么是一 .csproj 文件？
具有 CSPROJ 扩展名的文件表示 C# 项目文件，其中包含项目中包含的文件列表以及对系统程序集的引用。在 Microsoft VIiual Studio 中启动新项目时，您将获得一个 .csproj 文件以及主要解决方案 ([.sln](/zh/programming/sln/)) 文件。如果一个项目中有多个程序集，那么项目文件的数量也会相同，其中 .sln 文件将它们作为项目的一部分将它们联系在一起。该文件的内容定义了构建项目所需的所有要求，例如要包含的内容、平台要求、版本信息、Web 服务器或数据库服务器设置以及必须执行的任务。项目文件的内容以 XML 文件格式排列，可以在任何文本编辑器中打开以进行编辑和查看。它还为项目文件提供了一个逻辑视图，以便正确安排。

## CSPROJ 文件格式 #

开发人员可以自己创建项目文件，也可以遵循 [MSBuild XML Schema](https://msdn.microsoft.com/library/5dy88c2e.aspx)。项目文件的开放和透明结构使应用程序开发人员可以对项目的构建和部署方式进行复杂和细粒度的控制。这样一个工程文件的内容，相互之间有着非常明确的关系。下图显示了此类项目文件的关键元素以及它们之间的关系。

![](https://docs.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file/_static/image2.png)

以下部分详细说明了项目文件的文件格式元素。

### 项目元素###

[Project](https://msdn.microsoft.com/library/bcxfsh87.aspx) 元素是每个项目文件的根元素。它标识项目文件的 XML 模式，并且可以包含属性以指定构建过程的入口点。

```
<Project ToolsVersion#"4.0" DefaultTargets#"FullPublish"
        xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
</Project>
```

### 属性和条件

属性表示构建项目所需的必要信息。此类属性在 [PropertyGroup](https://msdn.microsoft.com/library/t4w159bs.aspx) 元素中定义。这些属性由键值对组成，其中属性元素名称定义属性键，元素的内容定义属性值。例如，您可以定义名为 ServerName 和 ConnectionString 的属性来存储静态服务器名称和连接字符串。

```
<PropertyGroup>    
 <ServerName>FABRIKAM\TEST1</ServerName>
 <ConnectionString>
     Data Source#FABRIKAM\TESTDB;InitialCatalog#ContactManager,...
 </ConnectionString>
</PropertyGroup>
```

可以通过元素指定条件，以指定评估元素的标准。这是在定义属性时由条件字指定的，如下所示：

```
<PropertyGroup>
<OutputRoot Condition#" '$(OutputRoot)'##'' ">..\Publish\Out\</OutputRoot>
   ...
</PropertyGroup>
```

当 MSBuild 处理此属性定义时，它首先检查 **$(OutputRoot)** 属性值是否可用。如果属性值为空（换句话说，用户没有为此属性提供值），则条件评估为 **true** 并且属性值设置为 **..\Publish\Out.**

### 项目和项目组

项目文件定义了构建过程的输入，这些输入实际上是不同的文件类型。在 MSBuild 命名法中，这些输入由 Item 元素表示并在 [ItemGroup](https://msdn.microsoft.com/library/646dk05y.aspx) 元素中定义。就像 **Property** 元素一样，您可以随意命名 **Item** 元素。但是，您必须指定 **Include** 属性来标识项目所代表的文件或通配符。

```
<ItemGroup>
<ProjectsToBuild Include#"$(SourceRoot)ContactManager-WCF.sln"/>
</ItemGroup>
```

### 目标和任务

[Task](https://msdn.microsoft.com/library/77f2hx1s.aspx) 元素表示单个构建指令（或任务）。 MSBuild 包含大量预定义任务。例如：

* **Copy** 任务将文件复制到新位置。
* **Csc** 任务调用 Visual C# 编译器。
* **Vbc** 任务调用 Visual Basic 编译器。
* **Exec** 任务运行指定的程序。
* **Message** 任务将消息写入记录器。

任务必须始终包含在 [Target](https://msdn.microsoft.com/library/t50z2hka.aspx) 元素中。 **Target** 元素是一组按顺序执行的一个或多个任务，一个项目文件可以包含多个目标。

```
<Project xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
<Target Name#"LogMessage">
 <Message Text#"Hello world!" />
</Target>
</Project>
```

## 参考

* [了解项目文件 - MSDN](https://docs.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-文件）

