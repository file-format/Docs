{
  "date" : "2019-12-12",
  "keywords" : [ "LRF", "file", "extension", "format", "eBook", "Digital book" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about LRF file format and APIs that can create and open LRF files.",
  "title" : "LRF File Format - A Sony Portable Reader File",
  "linktitle" : "LRF",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
    }
  },
  "lastmod" : "2019-12-12"
}

## What is an LRF file?

A file with .lrf extension is a Broad Band eBook (BBeB)file that contains data for a Sony BBeB, including text, images and pagination data. The file is saved in a compressed binary format which contains a header, a specified number of objects, and an object index. LRF and LRX files enclose the two BBeB book formats available. The LRF files are not encrypted and can be compiled from [LRX](/ebook/lrf/) files. The LRF files can be converted from several other file types including PDF and HTML. If your computer cannot open the LRF file, then you probably do not have the software installed to open or edit the LRF files. Programs that can open LRF files are Caliber, BookDesigner, Makelrf and Canon Book Creator for Windows, Caliber for Linux,  Caliber, and  Sony Reader for Macintosh.

## Brief History

LRF file type is first and foremost associated with Line Rider by [inXile entertainment](https://en.wikipedia.org/wiki/InXile_Entertainment). The Line Rider is an internet physics toy and was invented in September 2006 by a Slovenian university student, Boštjan Čadež. Sony brand eBook eReaders (such as Sony PRS-500 readers and Sony Librie) utilize the LRF file extension for their documents and texts. This proprietary file type is now obsolete, as well as the related LRS and LRX files. Those three file types made up the BroadBand eBook (BBeB) which was discontinued in 2010 when Sony began selling their ebooks in the EPUB format.

## LRF File Format

Detailed specifications of LRF file format are available at [web archive](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat). An LRF file consists of:
* a header
* a number of objects
* an object index.

All these values are in Intel (LSB first) order.

### LRF header

|Offset (hex)	|Size(bytes)	|Name/meaning|	Example value|
---|---|---|---|
|0	|8|	LRF Signature|	4C 00 52 00 46 00 00 00 = "LRF" in Unicode|
|8	|2|	version?|	999 in most files|
|A	|2|	"Psuedo-Encryption" |key byte	48|
|0C	|4|	RootObjectID|	0x0044|
|10	|8|	NumberOfObjects	|342|
|18	|8|	ObjectIndexOffset|	0x00093440|
|20	|4|	unknown|	0|
|24	|1|	Flags| (16 - back to front, 1 = front to back)	16|
|25	|1|	unknown |(padding?)	0|
|26	|2|	unknown|	1600|
|28	|2|	unknown| (padding?)	0|
|2A	|2|	Height?|	600|
|2C	|2|	Width?|	800|
|2E	|1|	unknown|	24|
|2F	|1|	unknown |(padding?)	0|
|30	|0x14|	unknown|	zeroes|
|44	|4|	Object ID of only PlaneStream (0x1E) object|	0x0042|
|48	|4|	unknown	|0x1536|
|4C	|2|	XMLCompSize|	0x035C|


## References

* [LRF File Format](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat)
* [BBeB - By Wikipedia](https://en.wikipedia.org/wiki/BBeB)
