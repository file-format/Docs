{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "CR3-tiedostomuoto - Canon Raw 3 -kuvatiedosto",
  "description":"Opi CR3-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata CR3-tiedostoja.",
  "linktitle" : "CR3",
  "menu" : {
    "docs" : {
      "identifier":"image-cr3-fi",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## Mikä on CR3-tiedosto?

CR3-tiedosto on Canonin RAW-kuvatiedostomuoto, joka on luotu valituilla Canonin digitaalikameroilla. Canon esitteli sen korvaamaan CR2-tiedostomuodon, ja jotkin Canonin digitaaliset laitteet käyttävät sitä. CR3-tiedostot tallentavat kameran tallentamat alkuperäiset käsittelemättömät häviöttömät kuvatiedot. Näiden raakakuvien käyttö tarjoaa korkealaatuisia kuvia ja antaa valokuvaajille runsaasti tilaa editointiin. Pääkuvatietojen lisäksi CR3-tiedostot tallentavat kuvan metatietoa.

## CR3 tiedostomuoto

CR3-tiedostot tallennetaan levylle binääritiedostoina ISO-perusmediatiedostomuodossa (ISO/IEC 14496-12), ja ne sisältävät myös mukautetun [Canon tags](https://exiftool.org/TagNames/Canon.html#uuid). Se sisältää myös [Canon 'crx' codec](https://github.com/LibRaw/LibRaw/blob/master/src/decoders/crx.cpp), joka on sekoitus JPEG-LS:ää (Rice-Golomb + RLE-koodaus) ja JPEG-2000:ta (LeGall 5/3 DWT + kvantifiointi).

## CR3 mukautetut tunnisteet

CR3-tiedostot sisältävät mukautettuja tunnisteita eri tarkoituksiin. Jotkut näistä tunnisteista ovat seuraavat.

|Tagin tunnus| Tunnisteen nimi| Kirjoitettava |Arvot / Huomautukset|
---|---|---|---|
|'CCTP' |CanonCCTP| - |--> Canon CCTP -tunnisteet|
|'CMT1' |IFD0| - |--> EXIF-tunnisteet|
|'CMT2' |ExifIFD| - |--> EXIF-tunnisteet|
|'CMT3' |MakerNoteCanon| - |--> Canon Tags|
|'CMT4' |GPSIinfo| - |--> GPS-tunnisteet|
|'CNCV' |CompressorVersion| ei| |
|'CNOP' |CanonCNOP| - |--> Canon CNOP -tunnisteet|
|'CNTH' |CanonCNTH| - |--> Canon CNTH -tunnisteet|
|'THMB' |ThumbnailImage| ei| |

## Viitteet

 * [CR2-tiedostomuoto](http://lclevy.free.fr/cr2/)
 * [Canon-tunnisteet](https://exiftool.org/TagNames/Canon.html#uuid)

