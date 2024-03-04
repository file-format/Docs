{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "CR3 failo formatas – „Canon Raw 3“ vaizdo failas",
  "description":"Sužinokite apie CR3 failo formatą ir API, kurios gali kurti ir atidaryti CR3 failus.",
  "linktitle" : "CR3",
  "menu" : {
    "docs" : {
      "identifier":"image-cr3-lt",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## Kas yra CR3 failas?

CR3 failas yra Canon RAW vaizdo failo formatas, sukurtas pasirinktais Canon skaitmeniniais fotoaparatais. Jį pristatė Canon, kad pakeistų CR2 failo formatą, ir yra naudojamas kai kuriuose Canon skaitmeniniuose įrenginiuose. CR3 failai saugo originalius neapdorotus be nuostolių vaizdo duomenis, užfiksuotus fotoaparatu. Naudojant šiuos neapdorotus vaizdus gaunami aukštos kokybės vaizdai, o fotografams suteikiama daug vietos juos redaguoti. Be pagrindinių vaizdo duomenų, CR3 failai taip pat saugo metaduomenų informaciją apie vaizdą.

## CR3 failo formatas

CR3 failai saugomi diske kaip dvejetainis failas ISO bazinio laikmenos failo formatu (ISO/IEC 14496-12) ir taip pat apima tinkintą [Canon tags](https://exiftool.org/TagNames/Canon.html#uuid). Jame taip pat yra [Canon 'crx' codec](https://github.com/LibRaw/LibRaw/blob/master/src/decoders/crx.cpp), kuris yra JPEG-LS (Rice-Golomb + RLE kodavimas) ir JPEG-2000 (LeGall 5/3 DWT + kiekybinis nustatymas) derinys.

## CR3 tinkintos žymos

CR3 failuose yra pasirinktinių žymų įvairiems tikslams. Kai kurios iš šių žymų yra tokios.

|Žymos ID| Žymos pavadinimas| Rašoma |Vertės / Pastabos|
---|---|---|---|
|'CCTP' |CanonCCTP| - |--> Canon CCTP žymės|
|'CMT1' |IFD0| - |--> EXIF žymės|
|'CMT2' |ExifIFD| - |--> EXIF žymės|
|'CMT3' |MakerNoteCanon| - |--> Canon žymos|
|'CMT4' |GPSIinfo| - |--> GPS žymos|
|'CNCV' |Kompresoriaus versija| ne| |
|'CNOP' |CanonCNOP| - |--> Canon CNOP žymės|
|'CNTH' |CanonCNTH| - |--> Canon CNTH žymos|
|'THMB' |ThumbnailImage| ne| |

## Nuorodos

 * [CR2 failo formatas](http://lclevy.free.fr/cr2/)
 * [Canon žymos](https://exiftool.org/TagNames/Canon.html#uuid)

