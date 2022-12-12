{
  "date" : "2019-12-12",
  "keywords" :[ "KF8", "přípona", "soubor", "formát", "eKniha", "Formát souboru Kindle", "Struktura souboru AZW3" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souboru AZW3 a rozhraních API, která mohou vytvářet a otevírat soubory AZW3.",
  "title" :"Co je soubor AZW3?",
  "linktitle" : "AZW3",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-06-04"
}

## Co je soubor AZW3?

AZW3, také známý jako Kindle Format 8 (**KF8**), je upravená verze formátu digitálních souborů [AZW](/cs/ebook/azw/) elektronické knihy vyvinutého pro zařízení Amazon Kindle. Formát je vylepšením starších souborů AZW a používá se na zařízeních Kindle Fire pouze se zpětnou kompatibilitou pro formát souboru předchůdce, tj. [MOBI](/cs/ebook/mobi/) a AZW. Amazon představil formát KFX (KF verze 10) po KF8, který se používá na nejnovějších zařízeních Kindle. Soubory AZW3 mají typ internetového média application/vnd.amazon.mobi8-ebook. Soubory AZW3 lze převést do řady dalších formátů souborů, jako jsou [PDF](/cs/pdf/), [EPUB](/cs/ebook/epub/), [AZW](/cs/ebook/azw/), [DOCX](/cs/ textový procesor/docx/) a [RTF](/cs/textový procesor/rtf/).

## Formát souboru AZ3/KF8 ##

Soubory KF8 jsou binární povahy a zachovávají si strukturu formátu souboru MOBI jako soubor PDB. Jak již bylo zmíněno dříve, soubor KF8 může později obsahovat jak MOBI, tak novější verzi EPUB KF8. Interní podrobnosti formátu byly dekódovány pomocí [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack), což je skript Pythonu, který analyzuje konečnou zkompilovanou databázi a extrahuje z ní zdrojové soubory MOBI nebo AZW. Soubory AZW3 (KF8) cílí na verzi EPUB3 se zpětnou kompatibilitou také pro EPUB. KF8 zkompiluje soubory EPUB a vygeneruje binární strukturu založenou na formátu souboru PDB.

## Reference ##

* [KF8 – z Wikipedie](https://en.wikipedia.org/wiki/Kindle_File_Format)
* [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack)

