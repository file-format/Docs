{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CSPROJ",
  "description":"Learn about CSPROJ file format and APIs that can create and open CSPROJ files.",
  "linktitle" : "CSPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2019-09-10"
}

Files with CSPROJ extension represent a C# project file that contains the list of files included in a project along with the references to system assemblies. When a new project is initiated in Microsoft VIiual Studio, you get one .csproj file along with the main solution ([.sln](/programming/sln/)) file. If there are more than one assemblies in a project, there will be equal number of project files as well where the .sln file ties them all together as part of the project. The contents of this file define all the requirements that are required to build the project such as content to include, the platfrom requirements, versioning information, web server or database server settings, and the tasks that must be performed. Contents of a project file are arranged in XML file format and can be opened in any text editor for editing as well as viewing. It also gives a logical view to the project files for proper arrangement.

# **CSPROJ File Format** #

Developers can create project files by themselves as well honouring the [MSBuild XML Schema](https://msdn.microsoft.com/library/5dy88c2e.aspx). The open and transparent structure of project files lets application developers impose sophisticated and fine-grained control over how the projects are built and deployed. The contents of such a project file have a very clear relationship among themselves. The following figure shows key elements and the relationship between these for such a project file.

![](https://docs.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file/_static/image2.png)

The following sections elaborate the file format elements for a project file.

### **Project Element** ###

The [Project](https://msdn.microsoft.com/library/bcxfsh87.aspx) element is the root element of every project file. It identifies the XML schema for the project file and can include attributes to specify the entry points for the build process.

```
<Project ToolsVersion#"4.0" DefaultTargets#"FullPublish"
        xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
</Project>
```

### **Properties and Conditions** ###

Properties represent the necessary information required to build a project. Such properties are defined within a [PropertyGroup](https://msdn.microsoft.com/library/t4w159bs.aspx) element. These properties consist of key-value pairs where the property element name defines the property key and the content of the element defines the property value. For example, you could define properties named ServerName and ConnectionString to store a static server name and connection string.

```
<PropertyGroup>    
 <ServerName>FABRIKAM\TEST1</ServerName>
 <ConnectionString>
     Data Source#FABRIKAM\TESTDB;InitialCatalog#ContactManager,...
 </ConnectionString>
</PropertyGroup>
```

Conditions can be specified via elements in order to specify the criteria for evaluating the element. This is specified by Condition word while defining the property as shown below:

```
<PropertyGroup>
<OutputRoot Condition#" '$(OutputRoot)'##'' ">..\Publish\Out\</OutputRoot>
   ...
</PropertyGroup>
```

When MSBuild processes this property definition, it first checks to see whether an **$(OutputRoot)** property value is available. If the property value is blank—in other words, the user hasn't provided a value for this property—the condition evaluates to **true** and the property value is set to **..\Publish\Out.**

### **Items and Item Groups** ###

A project file defines inputs to the build process which are actually different file types. In MSBuild nomenclature, these inputs are represented by Item elements and are defined within an [ItemGroup](https://msdn.microsoft.com/library/646dk05y.aspx) element. Just like **Property** elements, you can name an **Item** element however you like. However, you must specify an **Include** attribute to identify the file or wildcard that the item represents.

```
<ItemGroup>
<ProjectsToBuild Include#"$(SourceRoot)ContactManager-WCF.sln"/>
</ItemGroup>
```

### **Targets and Tasks** ###

A [Task](https://msdn.microsoft.com/library/77f2hx1s.aspx) element represents an individual build instruction (or task). MSBuild includes a multitude of predefined tasks. For example:

* The **Copy** task copies files to a new location.
* The **Csc** task invokes the Visual C# compiler.
* The **Vbc** task invokes the Visual Basic compiler.
* The **Exec** task runs a specified program.
* The **Message** task writes a message to a logger.

 Tasks must always be contained within [Target](https://msdn.microsoft.com/library/t50z2hka.aspx) elements. A **Target** element is a set of one or more tasks that are executed sequentially, and a project file can contain multiple targets.

```
<Project xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
<Target Name#"LogMessage">
 <Message Text#"Hello world!" />
</Target>
</Project>
```

## **References** ##

* [Understanding the Project File - MSDN](https://docs.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file)
