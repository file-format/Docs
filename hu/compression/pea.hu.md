{
  "date" : "2021-04-21",
  "keywords" :[ "borsó fájl", "borsó fájl formátum", "mi a borsó fájl", "fájl", "borsó példa", "borsó fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PEA - PeaZip archív fájlformátum",
  "description":"További információ a PEA fájlformátumról és az API-król, amelyek PEA fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "PEA",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-21"
}

## Mi az a PEA fájl?

A .pea kiterjesztésű fájl, amely a Pack, Encrypt és Authenticate szavak rövidítése, egy [zip](/hu/compression/zip/) archívum, amelyet a [PeaZip](https://peazip.github.io/) archiváló szoftverrel hoztak létre. Tömörítéssel és többszörös kötetes kimenettel rendelkezik, és rugalmas biztonsági modellt kínál a hitelesített titkosításon és kriptográfián keresztül. Ez biztosítja az adatok titkosságát és hitelesítését is. A PeaZip segédprogram nyílt forráskódú motorként érhető el, amely a követelményeknek megfelelően különböző operációs rendszerekre fordítható.

## PEA fájlformátum

A [PEA fájlformátum specifikációi] (https://peazip.github.io/pea_help.pdf) nyilvánosan elérhetők a fejlesztők számára. A PEA archívumok rugalmas biztonsági modellel és redundáns integritás-ellenőrzéssel rendelkező bináris fájlok, amelyek az ellenőrző összegektől a kriptográfiailag erős hash-ekig terjednek. Ez a kommunikáció három különböző szintjét határozza meg az irányításra:

* Streamek – a tényleges kimeneti adatfolyam, amelyet több bemeneti fájl alkot, és több kimeneti kötetre írható
* Objektumok – a .pea archívumba küldött bemeneti fájlok és mappák
* Kötetek - kimeneti archív fájl, amely a felhasználó által meghatározott méretre bontható

Ezek mindegyike opcionális, és a felhasználói igényeknek megfelelően beépíthető. A PEA fájlformátum egyetlen adatfolyamot tud tárolni, amely korlátlan számú objektumot tartalmaz. Minden adatfolyam legfeljebb 2^64 bájt méretű.

A PEA fájlok opcionális integritás-ellenőrzést és hitelesített titkosítást kínálnak AES használatával EAX vagy HMAC módban, vagy Twofish és Serpent segítségével EAX módban.

### PEA archívum fejléce

Az archívum fejléce 10 bájtos, és a következőképpen épül fel.

|Bájtok|Leírás|
---|---|
|1 | Magic byte mező a fájlformátum egyértelművé tételéhez: $EA|
|1 | Verziószám|
|1 | Revíziószám|
|1 | Hangerőszabályzó séma|
|1 | Az OS deklarálása, ahol a stream épült|
|1 | OS dátum és idő kódolás deklarálása|
|1 | Objektumok deklarálása név karakterkódolás|
|1 | A CPU típusának (7 bites kódolású) és endiannessnek (msb-ben) deklarálása |
|1 | Jövőbeli használatra fenntartva|

## Hivatkozások

* [PEA fájlformátum specifikációi](https://peazip.github.io/pea_help.pdf)
* [PEA fájlformátum](https://peazip.github.io/pea-file-format.html#.pea_specifications)

