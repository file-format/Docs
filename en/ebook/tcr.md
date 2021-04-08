{
  "date" : "2021-03-09",
  "keywords" : [ "TCR", "Psion", "extension", "format", "E-Book" ],
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

In the Early 90's the TCR file format was introduced for the ancient **Psion Series 3** palmtop devices. The company used their platform specific compression and this format has very limited support for the text formatting. It is a ZVR based file format and provides comparatively better compression rate than PalmDOC. It also work very well with FontMachine. Although, the TCR file format belongs to a discontinued device, but still this file format can be read by using some e-readers such as ReadManiac, MicroReader, ReadM, and FBReader. This file format can also be viewed on desktop with Sumatra PDF and with the Calibre application in Windows and linux.

## Technical Details
Since the TCR file format is based on ZVR compressor which is capable to reduce many files by about 50% of their original size. The compression scheme used by zvr is a little bit old. The compressed file begins with a dictionary of the 256 possible symbols which might show in the compressed file. The dictionary contains a fixed alternative string for each of these symbols. Decompression has become very fast even in OPL, and it can begin at any point in the compressed file.

## How to open a TCR file?

If you are not being able to open the TCR file on your computer; there may be many causes. The most important cause is that TCR supported softwwares are not installed on your device. In this case you need to see the following points as a guideline:

- Install the well suited software to run the file.
- If still you are facing difficulty to open the .rzs file; you must check the version of the software and see either that is supporting .rzs files or not. Some files can be supported by the old version and some by the latest one so, must check the details.
- After installing the appropriate verion of e-reading software make sure that it is set as the default application to open TCR files.

## Softwares that can open the TCR files
The TCR files can be open in the following software:

|Operating System| Sofware|
---|---|
|Microsoft Windows|Calibre, Sumatra PDF|
|MacOS|Calibre|
|Linux|Calibre|

## Possible problems while opening the file

If you are not being able to open and run the TCR file; it doesn't mean that you do not have a suitable software installed on your device. There might be some other issues which prevent the file to work properly. The possible problems might be one of the following:

- Corruption of a TCR file.
- Wrong links to the TCR file in registry entries.
- Deleted description of the TCR from the Windows registry
- Corrupted installation of an application that supports the TCR format
- An infected TCR file with an undesirable malware.
- The computer does not have sufficient hardware resources to operate the TCR file.
- Drivers used by the computer to open a TCR file are out dated.




## References

* [TCR - By MobileRead](https://wiki.mobileread.com/wiki/TCR)
* [ZVR Compressed Text File Reader](https://iay.org.uk/zvr/)
