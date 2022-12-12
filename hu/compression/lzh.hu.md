{
  "date" : "2021-06-16",
  "keywords" :[ "LZH", "Compressed", "File", "Extension", "File Format", "Lempel-Ziv", "Haruyasu", "LHA" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZH fájlformátum",
  "description":"További információ az LZH fájlformátumról és az LZH-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "LZH",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-06-16"
}

## Mi az LZH fájl? ##

Az .lzh és .lha kiterjesztésű fájlok általában az archív tömörítési fájlformátumra vonatkoznak. Ez a fájlformátum megegyezik más fájltömörítési formátumokkal, például [ZIP](/hu/compression/zip/), [RAR](/hu/compression/rar/) stb. Ezeknek a fájlformátumoknak a fő célja a fájl méretének csökkentése. formátumban az egyszerű küldéshez, valamint a tömörített formában való együtt tartáshoz. Az AS más nyugati cégekkel összehasonlítva az LZH fájlok nagyon népszerűek Japánban, és általában videojáték-adatok tömörítésére használják. A Windows 7 LZH-bővítménye a Windows 7 japán verziójába van beépítve. A Microsoft először a Windows XP japán verziójához fejlesztette ki a Microsoft Compressed (LZH) Folder Add-on-t. Ez a fájlformátum a Lempel-Ziv és a Haruyasu algoritmus által használt tömörítési rendelkezésekkel és funkciókkal van megvalósítva

## LZH specifikáció ##

Az LZH archívum tömörítési módszere öt bájtos szöveges karakterláncként jelenik meg, például -lz1-. Ezek a tömörített fájl harmadik és hetedik bájtjai.

|Leírás|Leírás|
---|---|
|Bővítés | .lzh, .lha|
|Média típusa| application/x-lzh-compressed|
|Típuskód| "LHA_" (LHA-SZÓKÖZ)|
|UTI| public.archive.lha|
|Kidolgozó| Haruyasu Yoshizaki (Yoshi)|
|Típus| Tömörítés|
|Bővítve től| LArc|

## Problémák az LZH fájl megnyitásakor ##

Az alábbiakban felsorolunk néhány problémát, amelyek az LZH fájlformátum rossz működését okozhatják:
  

* Lehetséges, hogy a fájl sérült. A probléma megoldásához töltse le újra a fájlt, vagy kérje meg a feladót, hogy küldje el újra a fájlt
* A második ok a fertőzött fájl, ebben az esetben ellenőrizze a fájlt megfelelően
* Nem megfelelő hivatkozások az LZH fájlhoz
* Az LZH leírásának eltávolítása
* Nincs elég hardver erőforrás
* A berendezés elavult illesztőprogramjai

## Referenciák ##

* [LZH - By Wikipedia](https://en.wikipedia.org/wiki/LHA_(file_format))
