{
  "date" : "2019-12-12",
  "keywords" :[ "KF8", "extensie", "bestand", "format", "eBook", "Kindle-bestandsindeling", "AZW3-bestandsstructuur"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over AZW3-bestandsindelingen en API's die AZW3-bestanden kunnen maken en openen.",
  "title" :"Wat is een AZW3-bestand?",
  "linktitle" : "AZW3",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-06-04"
}

## Wat is een AZW3-bestand?

AZW3, ook bekend als Kindle Format 8 (**KF8**), is de aangepaste versie van de [AZW](/nl/ebook/azw/) digitale bestandsindeling voor e-boeken die is ontwikkeld voor Amazon Kindle-apparaten. De indeling is een verbetering van oudere AZW-bestanden en wordt alleen gebruikt op Kindle Fire-apparaten met achterwaartse compatibiliteit voor de voorouderlijke bestandsindeling, namelijk [MOBI](/nl/ebook/mobi/) en AZW. Amazon introduceerde het KFX-formaat (KF-versie 10) na KF8 dat wordt gebruikt op de nieuwste Kindle-apparaten. AZW3-bestanden hebben internetmedia-type application/vnd.amazon.mobi8-ebook. AZW3-bestanden kunnen worden geconverteerd naar een aantal andere bestandsindelingen zoals [PDF](/nl/pdf/), [EPUB](/nl/ebook/epub/), [AZW](/nl/ebook/azw/), [DOCX](/nl/ tekstverwerking/docx/), en [RTF](/nl/tekstverwerking/rtf/).

## AZ3/KF8-bestandsindeling ##

KF8-bestanden zijn binair van aard en behouden de structuur van een MOBI-bestandsformaat als PDB-bestand. Zoals eerder vermeld, kan een KF8-bestand later zowel uit een MOBI als uit een nieuwere KF8-versie van EPUB bestaan. De interne details van het formaat zijn gedecodeerd door [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack), een Python-script dat de uiteindelijke gecompileerde database parseert en MOBI- of AZW-bronbestanden eruit haalt. AZW3-bestanden (KF8) zijn gericht op de EPUB3-versie met achterwaartse compatibiliteit voor EPUB. KF8 compileert de EPUB-bestanden en genereert een binaire structuur op basis van het PDB-bestandsformaat.

## Referenties ##

* [KF8 - Door Wikipedia](https://en.wikipedia.org/wiki/Kindle_File_Format)
* [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack)

