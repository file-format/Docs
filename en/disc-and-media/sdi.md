{
  "date" : "2021-08-13",
  "keywords" : [ "sdi file", "sdi file format", "what is an sdi file", "file", "sdi example", "sdi file extension","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
   "toc" : true,
  "description" : "Learn about SDI file format and APIs that can create and open SDI files.",
  "title" : "SDI - Windows System Deployment Image File",
  "linktitle" : "SDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
    }
  },
  "lastmod" : "2021-08-13"
}

## What is an SDI file?
The file with .sdi extension contains a load blob,boot blob, and part blob; commonly used by Windows Embedded Studio to create RAM disks or boot disks for loading and installing Windows. The SDI is abbreviated for System Deployment Image. The Windows Embedded Studio is a program used for creating disk images for Windows. Actually this program contains SDI File Manager program and a command line tool called **sdimgr.exe**, both can be used to deply, create and edit SDI images.

## SDI file format
The SDI file format is widely used to enable the use of a virtual disk for booting a system. Some versions of Microsoft Windows enable **RAM booting**, which is important to load an SDI file into memory and then boot from it. The SDI file format also enable itself for network booting by using the PXE (Preboot Execution Environment). It is also being used for hard disk imaging. 
### SDI file sections
The SDI file itself can be sub divided into the following sections:
- **Boot BLOB**: This contains the actual boot program, STARTROM.COM. This is an analogous to the boot sector of a hard disk.
- **Load BLOB**: This typically contains NTLDR and is launched by the boot BLOB.
- **Part BLOB**: This contains the actual boot runtime; also includes the boot.ini and ntdetect.com files which should be located within the root directory of the runtime.
- **Disk BLOB**: This is flat HDD image starting with a MBR. It is used for hard drive imaging instead of booting. Also only Disk BLOBs can be mounted with Microsoft's utilities.


## References 

* [System Deployment Image - by Wikipedia](https://en.wikipedia.org/wiki/System_Deployment_Image)

