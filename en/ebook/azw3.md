{
  "date" : "2019-12-12",
  "keywords" : [ "KF8", "Kindle File Format", "AZW3 File Structure" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Your file format guide to know what is an AZW3 file and APIs that can create and open them.",
  "title" : "What is an AZW3 file?",
  "linktitle" : "AZW3",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
    }
  },
  "lastmod" : "2019-11-20"
}

AZW3, also known as Kindle Format 8 (**KF8**), is the modified version of the [AZW](/ebook/azw/) ebook digital file format developed for Amazon Kindle devices. The format is an enhancement to older AZW files and is used on Kindle Fire devices only with backward compatibility for the ancestor file format i.e. [MOBI](/ebook/mobi/) and AZW. Amazon introduced KFX (KF version 10) format after KF8 that is used on the latest Kindle devices. AZW3 files have internet media type application/vnd.amazon.mobi8-ebook. AZW3 files can be converted to a number of other file formats such as [PDF](https://wiki.fileformat.com/view/pdf/), [EPUB](https://wiki.fileformat.com/ebook/epub/), [AZW](/ebook/azw/), [DOCX](https://wiki.fileformat.com/word-processing/docx/), and [RTF](https://wiki.fileformat.com/word-processing/rtf/).

## KF8 Format ##

KF8 files are binary in nature and retain the structure of a MOBI file format as PDB file. As mentioned earlier, a KF8 file may consist of both a MOBI as well as newer KF8 version of ePub later. The internal details of the format have been decoded by [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack), which is a Python script that parses the final compiled database and extracts MOBI or AZW source files from it. AZW3 (KF8) files target ePub3 version with the backward compatibility for ePub as well. KF8 compiles the ePub files and generates a binary structure based on the PDB file format.

## How to create KF8 Files? ##

You can create KF8 files using the command-line software tool, KindleGen, provided by Amazon. The files thus generate comprise of both the older as well as new file format database for backward compatibility so that old Amazon Kindle readers should be able to open these files.

Kindle Preview is another application software that can be used to create KF8 files by compiling a source [ePub](/ebook/epub/) file which is essentially a [zip](/compression/zip/) archive comprising of human-readable files. 

## References ##

(((
* [KF8 - By Wikipedia](https://en.wikipedia.org/wiki/Kindle_File_Format)
* [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack)
)))

 