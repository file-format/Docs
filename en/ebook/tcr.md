{
  "date" : "2021-03-09",
  "keywords" : [ "TCR", "Psion", "extension", "format", "E-Book" ],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about TCR file format for the Psion 3 series and APIs that can create and open tcr files.",
  "title" : "TCR - ZVR Compressed Text File",
  "linktitle" : "TCR",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
    }
  },
  "lastmod" : "2021-03-09"
}

## What is a TCR file?

In the Early 90's the TCR file format was introduced for the ancient **Psion Series 3** palmtop devices. The company used their platform specific compression and this format has very limited support for the text formatting. It is a ZVR based file format and it provides comparatively better compression rate than PalmDOC.

## Technical Details
Since the TCR file format is based on ZVR compressor which is capable to reduce many files by about 50% of their original size. The compression scheme used by zvr is a little bit old. The compressed file begins with a dictionary of the 256 possible symbols which might show in the compressed file. The dictionary contains a fixed alternative string for each of these symbols. Decompression has become very fast even in OPL, and it can begin at any point in the compressed file.




## References

* [TCR - By MobileRead](https://wiki.mobileread.com/wiki/TCR)
* [ZVR Compressed Text File Reader](https://iay.org.uk/zvr/)
