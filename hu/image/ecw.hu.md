{
  "date" : "2021-26-08",
  "keywords" :[ "ecw fájl", "ecw fájl formátum", "mi az ecw fájl", "fájl", "ecw példa", "ecw fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ECW - Enhanced Compression Wavelet Image File",
  "description":"További információ az ECW fájlformátumról és az ECW-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "ECW",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-26-08"
}

## Mi az ECW fájl? ##
Az ECW-fájl egy térinformatikai adatokkal való használatra tervezett képből áll. A tartalmazó kép valójában az Enhanced Compression Wavelet formátumban létrehozott tömörített kép. Az ECW fájlokat általában műholdas térképvetítés és légifelvételek tárolására használják. A térinformatikai alkalmazások támogatása érdekében a térképvetítési információk beágyazhatók az ECW-fájlokba.

## ECW fájlformátum
Az ECW egy szabadalmaztatott képformátum, amely wavelet tömörítésen alapul; műholdfelvételekre és légifotózásra optimalizálva. Ez a formátum jelenleg a Hexagon AB Intergraph része, de alapvetően az Earth Resource Mapping fejlesztette ki. Az ECW egy veszteséges tömörítési formátum, amely a nagy méretű képeket finom, váltakozó kontraszttal tömöríti, miközben megőrzi azok vizuális minőségét.
 

### Tulajdonságok
Íme az ECW formátum néhány jellemző tulajdonsága:
- A térképvetítési információk hozzáadhatók az ECW fájlformátumhoz a térinformatikai alkalmazások támogatása érdekében.
- Akár 65 535 sáv képadatai, beleértve a rétegeket vagy színeket is tömöríthetők ECW fájlformátumba másodpercenként 25 MB feletti sebességgel.
- Az ECWP protokoll egy hatékony streaming protokoll, amelyet az ECW és JPEG2000 képek hálózaton keresztüli továbbítására használnak.
- Az ECW-t és a JPEG2000-t támogató gyors SDK ingyenesen elérhető asztali megvalósításhoz Linux, Windows és MacOSX rendszeren



## Referenciák ##

* [ECW (fájlformátum) – a Wikipédia által](https://en.wikipedia.org/wiki/ECW_(file_format))


