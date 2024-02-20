{
  "date": "2021-08-11",
  "keywords": [
    "wim file",
    "wim file format",
    "what is a wim file",
    "file",
    "wim example",
    "wim file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Muhammad Umar"
  },
  "draft": "false",
  "toc": true,
  "description": "Learn about WIM file format and APIs that can create and open WIM files.",
  "title": "WIM - Windows Imaging Format File",
  "linktitle": "WIM",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-wim"
    }
  },
  "lastmod": "2021-08-11"
}

## What is a WIM file?
The files with .wim extensions were first time seen in Windows Vista. The WIM belongs to a file based imaging format which was typically introduced in the Microsoft Windows Vista. It enables a single disk image to be deployed to various computer platforms. WIM files are used to manage files such as updates, drivers, and components without re-booting the operating system image.  AQ WIM file contains a set of files and associated metadata which is very similar to other disk file formats.

## WIM file formats
The WIM file format is not like sector-based formats such as VHD or IS, in-fact it is a file-based which means that the fundamental unit of information in a WIM is a file. The basic benefit of being file-based is that a single-instance storage of a file referenced multiple times in the filesystem tree and hardware independence.It reduces the overhead of opening and closing various files individually, because the files are stored inside a single WIM file. WIM files can store multiple disk images, which are referenced either by their unique name or by their numerical index.
### Support for compression algorithms
WIM supports following families of  compression algorithms in descending speed and ascending ratio:
- XPRESS
- LZX
- LZMS
- Solid-compression.
The first three families are LZ77-based while Solid-compression were introduced along with LZMS in WIMGAPI Windows 8 and DISM Windows 8.1.
### Tools for WIM file format
Following tools are usually support the WIM file format:

- **ImageX**: A command-line tool used to edit, create, and deploy Windows disk images in the Windows Imaging Format. Along with the relevant WIMGAPI, It is distributed as part of the free Windows Automated Installation Kit. Starting with Windows Vista, Windows Setup uses the WAIK API to install Windows.
- **DISM**: A tool introduced in Windows 7 and Windows Server 2008 R2 that can perform service related tasks on a Windows installation image, be it an online image  or an offline image within a folder or WIM file. this tool was capable in mounting and unmounting images, adding a device driver to an offline image and querying installed device drivers in an offline image.
 



## References 

* [Windows Imaging Format - by Wikipedia](https://en.wikipedia.org/wiki/Windows_Imaging_Format)

