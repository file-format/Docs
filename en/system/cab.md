{
  "date" : "2021-06-29",
  "keywords" : [ "CAB", "extension", "file", "format", "system", "Windows Cabinet File", "Microsoft", "Installer", "SetUp", "AdvPak" ],
  "author" : {
    "display_name" : "Sami Cheema"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CAB - Windows Cabinet File",
  "description":"Learn about CAB file format and APIs that can create and open CAB files.",
  "linktitle" : "CAB",
  "menu" : {
    "docs" : {
      "parent" : "system"
    }
  },
  "lastmod" : "2021-06-29"
}

## What is a CAB file? ##

A file with a .cab extension belongs to a windows cabinet file that belongs to the category of system files. It is a file that is saved in the archive file format in the versions of Microsoft Windows that support compressed data algorithms, such as the [LZX](/compression/lzx/), Quantum, and [ZIP](/compression/zip/). The file comes in vital use when a user or developer wants to contain and share software installation data and files. The features of lossless data compression and the digital certification included in these files make this file perfect for storing and sharing such files. It supports different Microsoft installers such as Device Installer, SetUp API, and AdvPak.

## Brief History ##

CAB file is a data compression file type that was developed by Microsoft. It was initially called "Diamond", but then it popularly became known as CAB file, short for the word "Cabinet"

## Technichal Specification ##

A CAB file can usually contain up to a maximum of 65535 folders, which can, in turn, contain a maximum of 65536 files each. The CAB file storage mechanism is time and space-efficient as it saves each folder as a compressed block instead of compressing and storing each file separately. Empty folders cannot be stored in CAB archive folders. CAB file was first developed by Microsoft and is used in various installers, such as InstallShield with a slightly different format. CAB files are commonly connected to self-extracting programs. Microsoft CAB files are easily recognizable due to their unique marker that helps in identifying the format. The unique marker for all Microsoft CAB files is a four-word prefix, MSCF. Seeing this code, a user can easily distinguish a Microsoft CAB file from other files and use it accordingly in compressors or versions. The files can be compressed with more software installations data, or the present data can be decompressed using the right software. 


## CAB Example ##

The following example illustrates the relationship between files and folders in a CAB file structure:

{{< figure src="../cab.png" alt="CAB File Format" >}}

## Reference ##

* [CAB - WIKIPEDIA](https://en.wikipedia.org/wiki/Cabinet_(file_format))