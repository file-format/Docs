{
  "date" : "2021-04-08",
  "keywords" :[ "lz4 fájl", "lz4 fájlformátum", "mi az lz4 fájl", "fájl", "lz4 példa", "lz4 fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZ4 - LZ4 tömörített fájlformátum",
  "description":"További információ az LBR fájlformátumról és az API-król, amelyek LZ4 fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "LZ4",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Mi az LZ4 fájl?

Az .lz4 kiterjesztésű fájl az [LZ4](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm)) tömörítést támogató alkalmazásokkal/segédprogramokkal létrehozott tömörített archív fájl. Az LZ4 algoritmus a sebesség és a tömörítési arány közötti kompromisszumra összpontosít. A tömörített LZ4 archívumok az LZ4 parancssori segédprogrammal hozhatók létre, és ugyanilyen módon kicsomagolhatók.

## LZ4 fájlformátum

Az LZ4 tömörítési algoritmuson alapuló LZ4 fájlformátum független a CPU típusától, az operációs rendszertől, a fájlrendszertől és a karakterkészlettől. Alkalmas fájltömörítésre és streaming tömörítésre az LZ4 algoritmus használatával. Az LZ4 formátum kezdeti implementációját [C](/hu/programming/c/) nyelven Yann Collet hajtotta végre 2011-ben, és fejlesztői hivatkozásként elérhető a [Github] oldalon (https://github.com/lz4/lz4) .

### LZ4 keretformátum

Az LZ4 fájlformátum általános felépítése az alábbiak szerint látható.

|MagicNb|F. Leíró| Blokk|(...)|EndMark |C. Ellenőrző összeg|
---|---|---|---|---|---|
|4 bájt| 3-15 bájt||| 4 bájt| 0-4 bájt|

#### Varázsszám

4 bájt, Little endian formátum. Érték: 0x184D2204

#### Keretleíró

A keretleíró 3 t0 15 bájtból áll, és a specifikációk legfontosabb része. A Magic_Number és Frame_Descriptor mezőket együtt LZ4 keretfejlécnek nevezik, mérete pedig 7 és 19 bájt között változik. Ez az alábbiak szerint történik.

|FLG| BD| (Tartalom mérete)| (Szótárazonosító)| HC|
---|---|---|---|---|
|1 bájt| 1 bájt| 0 - 8 bájt| 0 - 4 bájt| 1 bájt|

#### Adatblokkok

Minden adatblokk a következő sorrendet követi.

|Blokkméret| adat| (Block Checksum)|
---|---|---|
|4 bájt| |0 - 4 bájt|

#### EndMark

A blokkok folyama akkor ér véget, amikor az utolsó adatblokkot a 0x00000000 32 bites érték követi.

#### Tartalmi ellenőrző összeg

A Content_Checksum ellenőrzi a helyesen dekódolt tartalom érvényességét, és az xxHash-32 algoritmus eredményével hajtják végre. Az összes blokk sikeres átvitelének eredményét a megfelelő sorrendben és hiba nélkül érvényesíti.

## Hivatkozások

* [LZ4 keretformátum](https://github.com/lz4/lz4/blob/dev/doc/lz4_Frame_format.md)
* [LZ4 tömörítési algoritmus – Wikipédia](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm))

