{
  "date" : "2021-03-09",
  "keywords" : [ "TCR", "Psion", "extension", "format", "eBook" ],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about TCR file format for the Psion 3 series and APIs that can create and open tcr files.",
  "title" : "TCR - Psion Series 3 eBook File",
  "linktitle" : "TCR",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
    }
  },
  "lastmod" : "2021-03-09"
}

## What is a TCR file?

In the early '90s, the TCR file format was introduced for the ancient **Psion Series 3** palmtop devices. The company used its platform-specific compression and this format has very limited support for text formatting. It is a ZVR based file format and provides a comparatively better compression rate than PalmDOC. It also works very well with FontMachine. Although the TCR file format belongs to a discontinued device, still this file format can be read by using some eReaders. This file format can also be viewed on a desktop with Sumatra PDF and with the Calibre application in Windows and Linux.

## Technical Details

Since the TCR file format is based on a ZVR compressor which is capable to reduce many files by about 50% of their original size. The compression scheme used by over is a little bit old. The compressed file begins with a dictionary of the 256 possible symbols which might show in the compressed file. The dictionary contains a fixed alternative string for each of these symbols. Decompression has become very fast even in OPL, and it can begin at any point in the compressed file.

## Problems to open a TCR file ##

If you are not being able to open and run the TCR file; it doesn't mean that you do not have suitable software installed on your device. There might be some other issues that prevent the file to work properly. The possible problems might be one of the following:

- Corruption of a TCR file.
- Wrong links to the TCR file in registry entries.
- Deleted description of the TCR from the Windows registry
- Corrupted installation of an application that supports the TCR format
- An infected TCR file with undesirable malware.
- The computer does not have sufficient hardware resources to operate the TCR file.
- Drivers used by the computer to open a TCR file are outdated.




## References

* [TCR - By MobileRead](https://wiki.mobileread.com/wiki/TCR)
* [ZVR Compressed Text File Reader](https://iay.org.uk/zvr/)
