{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "CR3 filformat - Canon Raw 3 billedfil",
  "description":"Lær om CR3-filformat og API'er, der kan oprette og åbne CR3-filer.",
  "linktitle" : "CR3",
  "menu" : {
    "docs" : {
      "identifier":"image-cr3-da",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## Hvad er CR3 fil?

En CR3-fil er et Canon RAW-billedfilformat, der er oprettet af udvalgte Canon-digitalkameraer. Det blev introduceret af Canon for at erstatte CR2-filformatet og bruges af nogle af Canons digitale enheder. CR3-filer gemmer de originale ikke-behandlede tabsfri billeddata, som er optaget af kameraet. Brugen af disse rå billeder giver billeder i høj kvalitet og giver masser af plads til redigering for fotografer. Ud over hovedbilleddata gemmer CR3-filer også metadataoplysninger om billedet.

## CR3 filformat

CR3-filer gemmes på disken som binær fil i ISO Base Media File Format (ISO/IEC 14496-12) og inkluderer også brugerdefinerede [Canon tags](https://exiftool.org/TagNames/Canon.html#uuid). Det inkluderer også [Canon 'crx' codec](https://github.com/LibRaw/LibRaw/blob/master/src/decoders/crx.cpp), der er en blanding af JPEG-LS (Rice-Golomb + RLE-kodning) og JPEG-2000 (LeGall 5/3 DWT + kvantificering).

## CR3 brugerdefinerede tags

CR3-filer indeholder brugerdefinerede tags til forskellige formål. Nogle af disse tags er som følger.

|Tag ID| Tag Navn| Skrivbar |Værdier / Noter|
---|---|---|---|
|'CCTP' |CanonCCTP| - |--> Canon CCTP-tags|
|'CMT1' |IFD0| - |--> EXIF Tags|
|'CMT2' |ExifIFD| - |--> EXIF Tags|
|'CMT3' |MakerNoteCanon| - |--> Canon Tags|
|'CMT4' |GPSIinfo| - |--> GPS-mærker|
|'CNCV' |Kompressorversion| nej| |
|'CNOP' |CanonCNOP| - |--> Canon CNOP Tags|
|'CNTH' |CanonCNTH| - |--> Canon CNTH Tags|
|'THMB' |ThumbnailImage| nej| |

## Referencer

 * [CR2-filformat](http://lclevy.free.fr/cr2/)
 * [Canon-tags](https://exiftool.org/TagNames/Canon.html#uuid)

