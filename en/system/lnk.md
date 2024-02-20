{
  "date": "2021-07-15",
  "keywords": [
    "LNK",
    "extension",
    "file",
    "format",
    "system",
    "LNK file",
    "link",
    "LNK files",
    "LNK documents",
    "application",
    "programs"
  ],
  "author": {
    "display_name": "Sami Cheema"
  },
  "draft": "false",
  "toc": true,
  "title": "LNK - Link File Format",
  "description": "Learn about LNK file format and APIs that can create and open LNK files.",
  "linktitle": "LNK",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-lnk"
    }
  },
  "lastmod": "2021-07-15"
}

## What is an LNK file? ##

An LNK file, analogous to an identity on the Mac system, is a Windows alternative or "link" that serves as a connection to an original image document folder, or program. It contains the type, position, and filename of the shortcut destination, as well as the application that opens the target document and an additional shortcut key. 

In Windows, straight a file, folder, or executable program and choose Create shortcut. The location of the file format and the “Beginning” directory are two basic features of  LNK files. The file format of LNK files is masked, and a curved arrow indicates that they are shortcuts.

## LNK File Format ##

LNK file formats usually have the same icon as their destination files, but with the addition of a little curled arrow to show that the file points to a different location. When the shortcut is double-clicked, it behaves as if the user had double-clicked the actual file. 

LNK files containing application shortcuts can have properties that affect how the program runs. To change the attributes, right-click the shortcut file and choose **Properties**, then change the Target field.

Instead of being file extensions, LNK files are Windows Explorer extensions. As a terminal extension, .lnk documents can only be used in Windows Explorer to substitute a file, and they have other purposes in Windows Explorer besides serving as a shortcut to a local document. These files start with the letter "L" as well. 

While shortcuts link to specific files and directories when they are created, they may become inoperable if the target is changed to a different location. Explorer will begin to repair a shortcut folder that points to a dead target when it is opened.


## Technichal Specification ##

Only when the "Hide extensions for recognized file types" folder viewing setting is unchecked, Windows does not show the .lnk document extension for document shortcuts. While it is not advised, you can enable the file extension to be displayed by removing the "NeverShowExt" property from the HKEY_CLASSES_ROOT\lnk file Windows registry item. 

To do so, take these steps: 

*	Open "Registration Editor" by entering "Regedit" into the taskbar search field and choosing the program
*	In the application, navigate to the Computer\HKEY HKEY_CLASSES_ROOT\lnkfile location
*	Make a backup of the item by right-clicking it and choosing Export
*	Select and delete the "NeverShowExt" attribute
*	Windows should be restarted


## Reference ##

* [LNK - Wikipedia](https://en.m.wikipedia.org/wiki/Shortcut_(computing))