{
  "date" : "2021-04-23",
  "keywords": [ "RES File", "how to open a res file", "what is a res file", "extension", "format", "RES file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "RES - C++ Compiled Resource Script",
  "description":"Learn about RES file format with RES example and APIs that can create and open RES files.",
  "linktitle" : "RES",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2021-04-23"
}

## What is a RES file?
The file with .res suffix or extension can belong to many file format categories. Here we are discussing the RES file format which is a C++ Compiled Resource Script; a binary file created by the Microsoft Resource Compiler (rc) that contains resource data; based on the resource-definition file's contents; relevant to its parent software project. The .res file usually re-formatted into a resource object file to link it to the executable file of an application.

## RES file format
The RES file format belongs to the Microsoft Resource Compiler (rc). The resource compiler is a tool that compiles resources such as cursors, icons, menus, and dialog boxes, that your application uses. The resource files usually have a .res extension; contains resources, such as cursors, images, and version information. An RES file could be a 16 or 32-bit resource file.
## Resource file structure
A resource file contains a series of various resource entries. Each entry contains a resource header and relevant data. A resource header is usually DWORD-aligned in the file and contains the following:

- A **DWORD** to specify the size of the resource header
- A **DWORD** to specify the size of the resource data
- The resource type
- The resource name
- Additional resource information

The resource header structure defines the format of the RES file. The data for the resource follows the resource header. Some resources also add a resource-specific group header pattern to provide information about a group of resources. Following are some of the resource entry types and their description:

### Accelerator Table Resources
An accelerator table is a resource entry in a RES file without a group header. The **ACCELTABLEENTRY** pattern defines each entry in the accelerator table. A RES file may have Multiple accelerator tables.

### Cursor and Icon Resources
Although, the system considers each icon and cursor as a single file, but these are stored in RES files as a group of icon resources or a group of cursor resources. The file formats of icon and cursor resources are same. A resource group header follows all of the individual icon or cursor group components in the .res file.

### Dialog Box Resources
A dialog box is also realized as a resource entry in the RES file. It contains one **DLGTEMPLATE** dialog box header pattern and one **DLGITEMTEMPLATE** pattern for each specific control in the dialog box. The **DLGTEMPLATEEX** and the **DLGITEMTEMPLATEEX** patterns explain the format of extended dialog box resources.

### Font Resources
A menu resource contains a **MENUHEADER** pattern subsequently one or more **NORMALMENUITEM** or **POPUPMENUITEM** patterns, one for each menu item in the menu template. The **MENUEX_TEMPLATE_HEADER** and the **MENUEX_TEMPLATE_ITEM** patterns explains the format of extended menu resources.

### Message Table Resources
A message table consists of formatted text for display as an error message or in a message box. The main pattern in a message table resource is the **MESSAGE_RESOURCE_DATA** structure.

### Version Resources
The main pattern in a version resource is the **VS_FIXEDFILEINFO**. Additional patterns include the **VarFileInfo** to store language information related data, and **StringFileInfo** for custom string information.




## References

 * [Resource File Formats](https://learn.microsoft.com/en-us/windows/win32/menurc/resource-file-formats)
 
 
