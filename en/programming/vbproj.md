{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "VBPROJ",
  "description":"Learn about VBPROJ file format and APIs that can create and open VBPROJ files.",
  "linktitle" : "VBPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2020-09-10"
}

## What is a VBPROJ file?

A file with .vbproj extension is a Microsoft Visual Basic project file that is used by Microsoft's MSBuild engine to build the projects within a Visual Studio solution. It is similar to [CSPROJ](/programming/csproj/) file for .NET projects written in [C#](/programming/cs/). The MSBuild engine reads information contained in different groups from the VBPROJ files and generates the output file. A VBPROJ file can contain information related to global identifiers, classes, and properties that define the project. VBPROJ files can be opened and edited using Microsoft Visual Studio and any common text editor such as Notepad on Windows and MacOS Operating Systems.

## VBPROJ File Format

VBPROJ files are textual files that are written in [XML](/web/xml/) file format based on the [MSBuild XML Schema](https://docs.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019). A VBPROJ file contains information in the form of XML tags that define information related to that particular group of settings. It is highly recommended to open and edit these setting files in Microsoft Visual Studio IDE.

### VBPROJ Elements

The constituent elements of a VB Settings file are as shown in the following image.

{{< figure src="../vbproj.png" alt="VBPROJ File Format" >}}

The following table gives a brief description of these elements.

|Element|Description|
---|---|
|Project| Root element of every project file and can include attributes to specify the entry points for the build process in addition to identifying XML schema for the project file|
|Properties and Conditions| Properties consist of Key-value pairs and are defined wihtin a PropertyGroup element. The property element name represents the property key and the content of the element defines the property value.|
|Items and ItemGroups|Items in a project file are inputs to the build process such as files-code files, configuration files, command files, and others required as part of the build process. Items are and must be defined within an ItemGroup element.|
|Targets and Tasks| A Task element represents an individual build instruction (or task). MSBuild includes a multitude of predefined tasks such as Copy, CSC, VBC, Exec. Tasks must always be contained in a `Target` Element which is a set of one or more tasks that are executed sequentially, and a project file can contain multiple targets.|

## References

* [Understanding the Project File](https://docs.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file)
* [MSBuild Schema Elements](https://docs.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019)
