{
  "date" : "2021-06-30",
  "keywords" : [ "msi file", "MSI file format", "what is a msi file", "file", "msi example", "msi file extension","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about MSI file format and APIs that can create and open MSI files.",
  "title" : "MSI - Windows Installer Package File",
  "linktitle" : "MSI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
    }
  },
  "lastmod" : "2021-06-30"
}

## What is an MSI file?
An MSI file used to install and launch Windows programs; a complete package for Microsoft Windows that contains installation information for a typical software program, including essential files to be installed and  information about the installation location. The MSI files may also contain the package for software updates. MSI files are similar to [EXE](/executable/exe/), but EXE sometime may not include the installer information and the software program may run directly when execute the EXE file.

## MSI file format
Windows Installer is actually an API (Application Programming Interface) and software component of Microsoft Windows used for the installation, removal, and maintenance of a software program. The installation information, and the optional files, are packaged as installation packages and loosely relational databases structured as COM Structured Storages; well known as **MSI files**, having the .msi file extension. The packages with the file extension **.mst** contain **Transformation Scripts** of Windows Installer, files with the **.msm** extension contains **Merge Modules** and the file extension **.pcp** is used for **Patch Creation Properties**. Windows Installer becomes more advanced after having significant changes from its earlier versions, Setup API. A GUI framework and automatic generation of the un-installation sequence are the new features of Windows Installer. It has been considered now as an alternative to stand-alone executable installer frameworks.

### Logical structure of MSI packages
A package designates the installation of one or more full products and is generally identified by a **GUID**. A product is made up of one or multiple components and grouped into various features. The Windows Installer does not handle dependencies between various products simultaneously. The logical structure of packages consists of the following elements:

- **Products**: A single, installed, working program or set of multiple programs combined together is a product. A product is identified by a unique GUID.
- **Features**: May contain any number of components and other sub-features. Smaller packages can consist of a single feature.
- **Components**: Component is treated by Windows Installer as a unit; can contain program files, folders, registry keys, COM components, and shortcuts.
- **Key Paths**: A key path is a specific file, ODBC data source, or registry key that the package author specifies as critical for a given component.

## References 

* [Windows Installer - by Wikipedia](https://en.wikipedia.org/wiki/Windows_Installer)

