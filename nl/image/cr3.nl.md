{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CR3-bestandsindeling - Canon Raw 3-beeldbestand",
  "description":"Meer informatie over CR3-bestandsindelingen en API's die CR3-bestanden kunnen maken en openen.",
  "linktitle" : "CR3",
  "menu" : {
    "docs" : {
      "identifier":"image-cr3",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## Wat is een CR3-bestand?

Een CR3-bestand is een Canon RAW-beeldbestandsformaat dat is gemaakt door geselecteerde digitale camera's van Canon. Het werd door Canon geïntroduceerd om het CR2-bestandsformaat te vervangen en wordt door sommige digitale Canon-apparaten gebruikt. CR3-bestanden slaan de originele, niet-verwerkte, verliesvrije beeldgegevens op die door de camera zijn vastgelegd. Het gebruik van deze onbewerkte afbeeldingen levert afbeeldingen van hoge kwaliteit op en biedt voldoende ruimte voor bewerking aan fotografen. Naast de belangrijkste afbeeldingsgegevens, slaan CR3-bestanden ook metadata-informatie over de afbeelding op.

## CR3-bestandsindeling

CR3-bestanden worden op schijf opgeslagen als binair bestand in de ISO Base Media File Format (ISO/IEC 14496-12) en bevatten ook aangepaste [Canon-tags](https://exiftool.org/TagNames/Canon.html#uuid). Het bevat ook de [Canon 'crx'-codec](https://github.com/LibRaw/LibRaw/blob/master/src/decoders/crx.cpp) die een mix is van JPEG-LS (Rice-Golomb + RLE codering) en JPEG-2000 (LeGall 5/3 DWT + kwantificering).

## CR3 aangepaste tags

CR3-bestanden bevatten aangepaste tags voor verschillende doeleinden. Sommige van deze tags zijn als volgt.

|Tag-ID| Tagnaam| Beschrijfbaar |Waarden/notities|
---|---|---|---|
|'CCTP' |CanonCCTP| - |--> Canon CCTP-tags|
|'CMT1' |IFD0| - |--> EXIF-tags|
|'CMT2' |ExifIFD| - |--> EXIF-tags|
|'CMT3' |MakerNoteCanon| - |--> Canon-tags|
|'CMT4' |GPSInfo| - |--> GPS-tags|
|'CNCV' |CompressorVersie| nee| |
|'CNOP' |CanonCNOP| - |--> Canon CNOP-tags|
|'CNTH' |CanonCNTH| - |--> Canon CNTH-tags|
|'THMB' |ThumbnailImage| nee| |

## Referenties

* [CR2-bestandsindeling](http://lclevy.free.fr/cr2/)
* [Canon-tags](https://exiftool.org/TagNames/Canon.html#uuid)

