{
  "date" : "2019-10-11",
  "keywords" :[ "gbr fájl", "gbr fájl formátum", "mi az a gbr fájl", "fájl", "gbr példa", "gbr fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GBR fájlformátum - Gerber fájlformátum PCB-hez",
  "description":"További információ a GBR fájlformátumról és az API-król, amelyek GBR-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "GBR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a GBR fájl?

A .gbr kiterjesztésű fájl egy Gerber képfájl formátum a nyomtatott áramköri lapok (PCB) tervezési adatátviteléhez. Az Ucamco fejlesztette ki. A NYÁK-tervezési adatok a fő összetevő, amelyet a gyártási ipar igényel a kezeléshez. A GRB-fájl PCB-adatokat tartalmaz, például rézrétegeket, forrasztómaszkot, jelmagyarázatot, valamint fúrási és útvonaladatokat. Használható olyan adatok átvitelére, mint például a PCB gyártási jellemzői, beleértve a vastagságot vagy a kikészítést szabványos formátumban. Minden NYÁK-tervező rendszer Gerber-fájlokat ad ki, amelyeket a PCB-gyártó rendszerek kezelhetnek. A GBR fájlok mára a nyomtatott áramköri lapok (PCB) tervezési adatátvitelének de facto szabványává váltak. Az Ucamco [ingyenes online megjelenítőt] (https://gerber-viewer.ucamco.com/) biztosít a GBR fájlformátumok megnyitásához és megtekintéséhez.

## GBR fájlformátum

A GBR egy UTF-8 ember által olvasható formátum, amely mindössze 27 parancsból áll. A parancsok e rövid listája és tömörsége miatt a GBR könnyen hibakereshető. A Gerber lényegében egy nyílt vektoros formátum 2D bináris képekhez. A metainformációk a képekkel együtt az Attribútumokon keresztül kerülnek átvitelre. Egyetlen GRB-fájl egyetlen képet határoz meg, és nincs szükség kísérőfájlok vagy külső paraméterek értelmezésére. Egy képhez csak egy fájl szükséges. 7 bites ASCII karaktereket használ a specifikációban meghatározott összes nyomtatható parancshoz és névhez. Ez teljes mértékben lefedi a teljes képgenerálást.

### Példa GBR fájl

Az alábbiakban egy példa a Gerber fájlra, amely egy 1,5 mm átmérőjű kört hoz létre az origó közepén. Soronként egy parancs van.

```
%FSLAX26Y26*%
%MOMM*%
%ADD   100C,1.5*%
D100* X0Y0D03*
M02*
```

## Hivatkozások

* [Gerber formátum](https://www.ucamco.com/en/gerber)

