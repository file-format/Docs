{
  "date" : "2019-10-11",
  "keywords" : [ "vcxproj", "file", "extension", "file format", "Visual C++ Project", "Programming Guide" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "VCXPROJ",
  "description":"Learn about VCXPROJ file format and APIs that can create and open VCXPROJ files.",
  "linktitle" : "VCXPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2020-09-10"
}

## What is a VCXPROJ file?

A file with .vcxproj extension is a Microsoft Visual C++ project file that stores the [C++](/programming/cpp/) project information. It contains information that is used by the MSBuild project system to compile and build the final output. VCXPROJ of Visual C++ projects is the same as that of [CSPROJ](/programming/csproj/) for .NET projects. VCXPROJ files do not contain any code but refers to all the classes, targets and properties defined for the project to build the project. These can be opened in plain text editors or preferably in Microsoft Visual Studio IDE.


## VCXPROJ File Format - More Information

VCXPROJ files are text files that are created in [XML](/web/xml/) file format. These can be opened in any text editor but it is highly recommended to use Microsoft Visual Studio IDE for opening and editing these files. These weren't designed for manual editing. Mistakes can cause the IDE to crash or behave in unexpected ways.

The contents of a sample VCXPROJ file are as follow.

```
<Project DefaultTargets="Build" ToolsVersion="4.0" xmlns='http://schemas.microsoft.com/developer/msbuild/2003'>
  <ItemGroup Label="ProjectConfigurations" />
  <PropertyGroup Label="Globals" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.default.props" />
  <PropertyGroup Label="Configuration" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.props" />
  <ImportGroup Label="ExtensionSettings" />
  <ImportGroup Label="PropertySheets" />
  <PropertyGroup Label="UserMacros" />
  <PropertyGroup />
  <ItemDefinitionGroup />
  <ItemGroup />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.targets" />
  <ImportGroup Label="ExtensionTargets" />
</Project>
```
### VCXPROJ File Elements

A typical VCXPROJ file contains a number of elements as can be seen in the example XML above. The [VCXPROJ structure](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160) by Microsoft explains each file element in detail and can be referred from developer's perspective.

#### Project Element

This is the root node of the VCXPROJ file. MSBuild uses this element to read the build version and default target for compilation.

#### ProjectConfigurations ItemGroup Element

It contains the project configuration information that can include the build method (Debug or Release), 32 or 64-bit compilation, optimization options, and others. Information in this group is used by IDE to load the project.

#### ProjectConfiguration Elements

The ProjectConfiguration elements in a VCXPROJ file containns information about the build and platform for which the project is loaded. Its name should follow the format `$(Configuration)|$(Platform)`.

#### Globals PropertyGroup Element

This section contains settings that provide information for project level such as:

 * ProjectGuid
 * RootNamespace
 * ApplicationType or ApplicationTypeRevision


## References

* [VCXPROJ Structure - MSDN](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160)
* [C++ Project Files](https://learn.microsoft.com/en-us/cpp/build/reference/project-files?view=msvc-160)
