{
  "date" : "2019-12-12",
  "keywords" :[ "KF8", "extension", "file", "format", "eBook", "Kindle File Format", "AZW3 File Structure" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ az AZW3 fájlformátumról és az API-król, amelyek AZW3 fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"What is an AZW3 file?",
  "linktitle" : "AZW3",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-06-04"
}

## Mi az AZW3 fájl?

Az AZW3, más néven Kindle Format 8 (**KF8**), az [AZW](/hu/ebook/azw/) ebook digitális fájlformátum módosított változata, amelyet Amazon Kindle eszközökhöz fejlesztettek ki. A formátum a régebbi AZW-fájlok továbbfejlesztése, és csak a Kindle Fire-eszközökön használják visszafelé az ősfájlformátummal, azaz a [MOBI](/hu/ebook/mobi/) és az AZW-vel. Az Amazon bevezette a KFX (KF 10-es verzió) formátumot a KF8 után, amelyet a legújabb Kindle eszközökön használnak. Az AZW3 fájlok internetes médiatípusú application/vnd.amazon.mobi8-ebook. Az AZW3 fájlok számos más fájlformátumba konvertálhatók, például [PDF](/hu/pdf/), [EPUB](/hu/ebook/epub/), [AZW](/hu/ebook/azw/), [DOCX](/hu/ szövegszerkesztő/docx/), és [RTF](/hu/word-processing/rtf/).

## AZ3/KF8 fájlformátum ##

A KF8 fájlok bináris jellegűek, és megtartják a MOBI fájlformátum szerkezetét PDB fájlként. Ahogy korábban említettük, a KF8-fájl MOBI-ból és később az EPUB újabb KF8-as verziójából is állhat. A formátum belső részleteit a [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack) dekódolta, amely egy Python-szkript, amely elemzi a végső lefordított adatbázist, és kibontja belőle a MOBI vagy AZW forrásfájlokat. Az AZW3 (KF8) fájlok az EPUB3 verziót célozzák meg, visszafelé kompatibilis EPUB-val is. A KF8 összeállítja az EPUB fájlokat, és létrehoz egy bináris struktúrát a PDB fájlformátum alapján.

## Referenciák ##

* [KF8 – a Wikipedia által](https://en.wikipedia.org/wiki/Kindle_File_Format)
* [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack)

