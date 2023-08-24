
{
  "date" : "2022-01-28",
  "keywords": [ ".aml file", "extension", "format","Microsoft Assistance Markup Language File", "how to open .aml file","aml file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "AML File - Microsoft Assistance Markup Language File",
  "description":"Learn about what is an AML file and APIs that can create and open AML files.",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier":"programming-aml",
      "parent" : "programming"
    }
  },
  "lastmod" : "2022-01-28"
}

# AML - Microsoft Assistance Markup Language File

## What is an AML file?

An AML (Assistance Markup Language) file is an XML file generated with Microsoft Assistance Markup Language (MAML). It was developed by Microsoft to provide online help for Microsoft Windows OS. Before this, Windows help was available in the compiled HTML [CHM](/web/chm/) file format. AML files provide a structured document that lets application create source code and supporting help pages. This allows the definition of documents and their constituent elements by their context. The AML help files are published online and can be configured to get updated from the package updates available online.

## MAML File Structure

AML files generated using MAML are saved as [XML](/web/xml/) files that can be used to express a wide range of active concepts. It can also provide guided help (active content wizard) that makes the help file interactive for user with step-by-step wizard.

An AML file generated using the MAML follows its authoring structure that can be divided into segments like:

 * Conceptual
 * FAQ
 * Glossary
 * Procedure
 * Reference
 * Reusable Content
 * Task
 * Troubleshooting, and
 * Tutorial

## How to create MAML Files?

MAML files can be created using one of the following methods:

 * Using Sandcastle - Utilizes a suite of schemas and program executables to generate the help file. This tool, however, has been discontinued.
 * Using DocProject - A Microsoft Visual Studio plugin that can be executed from within Microsoft Visual Studio for generating the help content.

MAML files can be created using Sandcastle, a suite of .XSL schemas and program executables. They may also be created using DocProject, a Microsoft Visual Studio help authoring tool add-in.

## References

 * [Create XML-based help using PlatyPS](https://learn.microsoft.com/en-us/powershell/scripting/dev-cross-plat/create-help-using-platyps?view=powershell-7.2)
 * [Microsoft Assistance Markup Language](https://en.wikipedia.org/wiki/Microsoft_Assistance_Markup_Language)

# AML - Arc Macro Language File

## What is an ARC Macro AML file?

An AML (ARC Macro Language) file is a scripting file generated with the ArcInfo Workstation GIS application. It is written in the ARC Macro Language, which is a proprietary high-level algorithmic language for creating GIS applications in ArcInfo. AML was designed by ESRI in 1986 and served the purpose of creating applications from their command line ARCINFO GIS system. Being scripting file, AML files can contain script commands to carry out a number of tasks such as creating user interface components and manipulate map data.

## AML File Format - More Information

AML, being scripting files, save the information to disc as plain text files. It follows the AML syntax that was based on the CPL shell language of the PRIMOS operating system. AML language has been replaced by ESRI's geoprocessing framework that is part of the ArcGIS suite and uses ArcObjects to provide programming support via VBA or Python.

## References

 * [ARC Macro Language](https://en.wikipedia.org/wiki/ARC_Macro_Language)
 * [Using AML with Script Tools](https://desktop.arcgis.com/en/arcmap/latest/analyze/creating-tools/using-amls-with-script-tools.htm)
