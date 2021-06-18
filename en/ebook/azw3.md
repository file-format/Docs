{
  "date" : "2019-12-12",
  "keywords" : [ "KF8", "extension", "file", "format", "eBook", "Kindle File Format", "AZW3 File Structure" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about AZW3 file format and APIs that can create and open AZW3 files.",
  "title" : "What is an AZW3 file?",
  "linktitle" : "AZW3",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
    }
  },
  "lastmod" : "2021-06-04"
}

## What is an AZW3 file?

AZW3, also known as Kindle Format 8 (**KF8**), is the modified version of the [AZW](/ebook/azw/) ebook digital file format developed for Amazon Kindle devices. The format is an enhancement to older AZW files and is used on Kindle Fire devices only with backward compatibility for the ancestor file format i.e. [MOBI](/ebook/mobi/) and AZW. Amazon introduced KFX (KF version 10) format after KF8 that is used on the latest Kindle devices. AZW3 files have internet media type application/vnd.amazon.mobi8-ebook. AZW3 files can be converted to a number of other file formats such as [PDF](/pdf/), [EPUB](/ebook/epub/), [AZW](/ebook/azw/), [DOCX](/word-processing/docx/), and [RTF](/word-processing/rtf/).

## AZ3/KF8 File Format ##

KF8 files are binary in nature and retain the structure of a MOBI file format as PDB file. As mentioned earlier, a KF8 file may consist of both a MOBI as well a newer KF8 version of EPUB later. The internal details of the format have been decoded by [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack), which is a Python script that parses the final compiled database and extracts MOBI or AZW source files from it. AZW3 (KF8) files target EPUB3 version with the backward compatibility for EPUB as well. KF8 compiles the EPUB files and generates a binary structure based on the PDB file format.

## References ##

* [KF8 - By Wikipedia](https://en.wikipedia.org/wiki/Kindle_File_Format)
* [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack)
