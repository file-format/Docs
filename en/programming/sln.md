{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "SLN",
  "linktitle" : "SLN",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2019-09-10"
}

A file with .SLN extension represents a Visual Studio solution file that keeps information about the organization of projects in a solution file. The contents of such a solution file are written in plain text inside the file and can be observed/edited by opening the file in any text editor. The information contained in a solution file remains persistent and is used to load the information associated with the solution such as [projects ](/programming/csproj/)and any other required information. The project files referenced by the solution file contain additional information to enable the environment for populating the hierarchy with that project's items. No data is stored in the .sln file, although project information can be written to the .sln file if required.

## **SLN Versions History** ##

The solution format version has evolved with each Microsoft Visual Studio solution with the passage of time. The details about these are as follow. 


|**Visual Studio Version**|**Solution Format Version**
|2003|8.00
|2005|9.00
|2008|10.00
|2010|11.00
|2013|12.00
|2015|12.00
|2017|12.00

### **Contents of a Solution File** ###

A solution file consists of several sections that are read by the environment to load the project. A sample .sln file contents are as shown below.

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

### **Project Declaration** ###

A solution file can contain more than one projects declaration and that too of difference project types. For example, a single solution file can contain a CSharp as well as a VB.NET project. These types are distinguished in a solution using the [Project-Type-GUID](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs). The above project declaration can be generalized as follow for clear understanding.

```
Project("{Project-Type-GUID}") # "Project-Name", "Project-Path.extension", "{Project-GUID}"
```

**Project-Type-GUID: **The Project-Type-GUID is unique for different project types and is used by the solution reader to identify the type of project. In this case, F184B08F-C81C-45F6-A57F-5ABD9991F28F shows that it is a VB.NET project. 

**Project GUID: **The unique GUID of the project that differentiates it from other projects in the solution. The unique ID of a project in the solution makes it possible for other projects in the solution to access it. 

Based on the information contained in the project section of the .sln file, the environment loads each project file. The project itself is then responsible for populating the project hierarchy and loading any nested projects. Any changes made to the solution are saved back to the solution file upon saving or closing the project. 

### **References** ###

* [Solution File - By MSDN](https://docs.microsoft.com/en-us/visualstudio/extensibility/internals/solution-dot-sln-file?view#vs-2017)
* [Project Type GUIDs](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs)