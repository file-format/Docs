{
  "date" : "2021-09-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "IPR File Format - IntelliJ IDEA Project File",
  "description":"Learn about IPR file format and APIs that can create and open IPR files.",
  "linktitle" : "IPR",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2021-09-13"
}

## What is an IPR file?

IPR file is a project file created with the Java IDE **IntelliJ IDEA**. All the information related to project settings such as directory structure, source code files, libraries included in the project, and compiler settings are stored in the IPR files. When a project is opened from within IntelliJ IDEA, the IDE reads the information in the IPR file and loads the corresponding files and settings. IPR files have been replaced by the .IDEA files that contains all the information as Settings Directory.

## IPR File Format

IPR files are saved in the universally understandable [XML](/web/xml/) file format that is human readable. It contains all the project related information in tags that are loaded for displaying project related contents.

Since IPR files are stored in XML file format, these can be opened in any text editor such as Notepad, Notepad++, Atom, and Apple TextEdit.

## Reference ##

* [Creating an Managing Projects - IntelliJ IDEA](https://www.jetbrains.com/help/idea/creating-and-managing-projects.html)
