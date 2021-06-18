{
  "date" : "2021-06-16",
  "keywords" : [ "LZH", "Compressed", "File", "Extension", "File Format", "Lempel-Ziv", "Haruyasu", "LHA" ],
  "author" : {
    "display_name" : "Sami Cheema"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "LZH File Format",
  "description":"Learn about LZH file format and APIs that can create and open LZH files.",
  "linktitle" : "LZH",
  "menu" : {
    "docs" : {
      "parent" : "compression"
    }
  },
  "lastmod" : "2021-06-16"
}

## What is an LZH file? ##

A file with .lzh and .lha extension usually relates to archive compression file format. This file format is the same as other file compression formats like [ZIP](/compression/zip/), [RAR](/compression/rar/), etc. The main purpose of these file formats is to reduce the size of the format for easily sending as well as to keep them together in compressed form. AS compare to other western companies LZH files are very popular in Japan and usually used for compressing video game data. The LZH add-on for Windows 7 is built into the Japanese version of Windows 7. Microsoft first released the Microsoft Compressed (LZH) Folder Add-on for the Japanese version of Windows XP. This file format is implemented with compression provisions and features used by the Lempel-Ziv and Haruyasu algorithm

## Specification of the file ##

The compression method of an LZH archive is shown as a five-byte text string, such as -lz1-. These are the third through seventh bytes in the compressed file.

|Specification|Description|
---|---|
|Extension	| .lzh, .lha|
|Media Type| application/x-lzh-compressed|
|Type Code|	"LHA_" (L-H-A-SPACE)|
|UTI|	public.archive.lha|
|Developed By|	Haruyasu Yoshizaki (Yoshi)|
|Type|	Compression|
|Extended from|	LArc|

## Problems to Open an LZH file ##

Following are the few problems that may cause poor working of LZH file format:
  
  *	 The file may be corrupt. To solve this issue, download the file again or ask the sender to resend the file again
  *	 The second reason is infected file in this case scan the file properly
  *	 Improper links to the LZH file 
  *	 Removal of the description of the LZH 
  *	 Not enough  hardware resources
  *	 Outdated drivers of the equipment

## References ##

* [LZH - By Wikipedia](https://en.wikipedia.org/wiki/LHA_(file_format))