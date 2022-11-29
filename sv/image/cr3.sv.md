{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CR3-filformat - Canon Raw 3-bildfil",
  "description":"Läs mer om CR3-filformat och API:er som kan skapa och öppna CR3-filer.",
  "linktitle" : "CR3",
  "menu" : {
    "docs" : {
      "identifier":"image-cr3",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## Vad är CR3 fil?

En CR3-fil är ett Canon RAW-bildfilformat som skapas av utvalda Canons digitalkameror. Det introducerades av Canon för att ersätta filformatet CR2 och används av några av Canons digitala enheter. CR3-filer lagrar den ursprungliga obearbetade förlustfria bilddata som tagits av kameran. Användningen av dessa råbilder ger bilder av hög kvalitet och ger gott om utrymme för redigering för fotografer. Förutom huvudbilddata lagrar CR3-filer även metadatainformation om bilden.

## CR3 filformat

CR3-filer lagras på skiva som binär fil i ISO Base Media File Format (ISO/IEC 14496-12) och inkluderar även anpassade [Canon-taggar](https://exiftool.org/TagNames/Canon.html#uuid). Den innehåller också [Canon 'crx'-codec](https://github.com/LibRaw/LibRaw/blob/master/src/decoders/crx.cpp) som är en blandning av JPEG-LS (Rice-Golomb + RLE) kodning) och JPEG-2000 (LeGall 5/3 DWT + kvantifiering).

## CR3 anpassade taggar

CR3-filer innehåller anpassade taggar för olika ändamål. Några av dessa taggar är följande.

|Tagg-ID| Taggnamn| Skrivbar |Värden / Noteringar|
---|---|---|---|
|'CCTP' |CanonCCTP| - |--> Canon CCTP-taggar|
|'CMT1' |IFD0| - |--> EXIF-taggar|
|'CMT2' |ExifIFD| - |--> EXIF-taggar|
|'CMT3' |MakerNoteCanon| - |--> Canon Tags|
|'CMT4' |GPSIinfo| - |--> GPS-taggar|
|'CNCV' |KompressorVersion| nej| |
|'CNOP' |CanonCNOP| - |--> Canon CNOP Tags|
|'CNTH' |CanonCNTH| - |--> Canon CNTH Tags|
|'THMB' |Miniatyrbild| nej| |

## Referenser

* [CR2-filformat](http://lclevy.free.fr/cr2/)
* [Canon-taggar](https://exiftool.org/TagNames/Canon.html#uuid)

