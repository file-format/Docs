{
  "date" : "2019-12-12",
  "keywords" :[ "KF8", "tillägg", "fil", "format", "eBook", "Kindle-filformat", "AZW3-filstruktur" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om AZW3-filformat och API:er som kan skapa och öppna AZW3-filer.",
  "title" :"Vad är en AZW3-fil?",
  "linktitle" : "AZW3",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-06-04"
}

## Vad är en AZW3 fil?

AZW3, även känt som Kindle Format 8 (**KF8**), är den modifierade versionen av [AZW](/sv/ebook/azw/) ebook digitala filformat utvecklat för Amazon Kindle-enheter. Formatet är en förbättring av äldre AZW-filer och används endast på Kindle Fire-enheter med bakåtkompatibilitet för förfaderns filformat, dvs. [MOBI](/sv/ebook/mobi/) och AZW. Amazon introducerade KFX (KF version 10) format efter KF8 som används på de senaste Kindle-enheterna. AZW3-filer har internetmediatyp application/vnd.amazon.mobi8-ebook. AZW3-filer kan konverteras till ett antal andra filformat som [PDF](/sv/pdf/), [EPUB](/sv/ebook/epub/), [AZW](/sv/ebook/azw/), [DOCX](/sv/ word-processing/docx/), och [RTF](/sv/word-processing/rtf/).

## AZ3/KF8 filformat ##

KF8-filer är binära till sin natur och behåller strukturen för ett MOBI-filformat som PDB-fil. Som nämnts tidigare kan en KF8-fil bestå av både en MOBI och en nyare KF8-version av EPUB senare. Formatets interna detaljer har avkodats av [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack), som är ett Python-skript som analyserar den slutliga kompilerade databasen och extraherar MOBI- eller AZW-källfiler från den. AZW3 (KF8)-filer är inriktade på EPUB3-versionen med bakåtkompatibilitet för EPUB också. KF8 kompilerar EPUB-filerna och genererar en binär struktur baserad på PDB-filformatet.

## Referenser ##

* [KF8 - av Wikipedia](https://en.wikipedia.org/wiki/Kindle_File_Format)
* [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack)

