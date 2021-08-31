{
  "date" : "2021-08-31",
  "keywords" : [ "xbe file", "xbe file format", "what is an xbe file", "file", "xbe example", "xbe file extension","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about XBE file format and APIs that can create and open XBE files.",
  "title" : "XBE - iOS Application Package File",
  "linktitle" : "XBE",
  "menu" : {
    "docs" : {
      "parent" : "executable"
    }
  },
  "lastmod" : "2021-08-31"
}

## What is an XBE file?
A file having .xbe extension is an executable application from an Xbox video game disc. The XBE files are the main files that are executed in the Xbox System and are not supposed to be opened typically on a computer, but it can be opened on a PC using an Xbox emulation program. These files are usually created by game developers, and then signed by Microsoft. The file structure is similar to the Windows PE files, but some important changes according to the XBox settings are applied to make it runnable at XBox.

## XBE file format
The XBE file is composed of an image header, a collection of section headers, a certificate, thread local storage data, a collection of library versions, Microsoft bitmap, and the sections that contain the code and resources.

### Image Header
The image header comprises the information that explains where the other components of the executable are located within the file, and how the runnable should be treated and loaded.

### TLS Table
The TLS Table consists of all the information needed by the XBE to properly set up thread-local storage. It is basically unique to the TLS Directory found in PE32 files, and can be directly copied from there. This table may be omitted, if the XBE file does not use any thread-local storage, and the respective field in the image header set to zero.

| Offset |  Size  |         Name         |                                        Description                                         |
--------|--------|----------------------|--------------------------------------------------------------------------------------------|
| 0x0000 | 0x0004 |    Raw Data Start    | Absolute (i.e. not an RVA) address of start of the TLS variable data in the program image. |
| 0x0004 | 0x0004 |     Raw Data End     |  Absolute (i.e. not an RVA) address of end of the TLS variable data in the program image.  |
| 0x0008 | 0x0004 |   Address of Index   |               Absolute (i.e. not an RVA) address of the TLS Index variable.                |
| 0x000C | 0x0004 | Address of Callbacks |  Absolute (i.e. not an RVA) address of the null-terminated TLS callback functions table.   |
| 0x0010 | 0x0004 |  Size of Zero Fill   |      The number of bytes following the raw data that should be set to zero in memory.      |
| 0x0014 | 0x0004 |   Characteristics    |                                    Describes alignment.                                    |

### Certificate

 A a certificate is mandatory for each Xbox executable that contains information about the titles:
 
- Time and date when the certificate was created
- Title ID
- Title name
- Alternative title IDs
- Allowed types of media that the executable can be run from (HD, DVD, CD, etc.)
- Game region
- Game ratings
- Disk number
- Version
- LAN key raw data used for System Link
- Signature key raw data (used to sign savegames)
- Alternate signature keys
- Original size of the certificate
- Online service name (not present in early executables)
- Run time security flags (not present in early executables)
 
### Allowed media types
Media types which are allowed by the executable to be run from. The following values are known:
|     Media type      |   Value    |
---------------------|------------|
|      HARD_DISK      | 0x00000001 |
|       DVD_X2        | 0x00000002 |
|       DVD_CD        | 0x00000004 |
|         CD          | 0x00000008 |
|      DVD_5_RO       | 0x00000010 |
|      DVD_9_RO       | 0x00000020 |
|      DVD_5_RW       | 0x00000040 |
|      DVD_9_RW       | 0x00000080 |
|       DONGLE        | 0x00000100 |
|     MEDIA_BOARD     | 0x00000200 |
| NONSECURE_HARD_DISK | 0x40000000 |
|   NONSECURE_MODE    | 0x80000000 |
|     MEDIA_MASK      | 0x00FFFFFF |

### Sections
The sections are expressed by the section headers. The section headers start right after the certificate and contain information where in the file the actual sections exists. At least two sections are always present in an Xbox executable: 
- .text 
- .rdata


## References 

* [Xbe - XBox Executable](https://xboxdevwiki.net/Xbe)

