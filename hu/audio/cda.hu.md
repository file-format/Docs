{
  "date" : "2021-06-09",
  "keywords" :[ "cda", "fájl", "kiterjesztés", "formátum", "mi az a cda fájl", "zene", "cda fájlformátum", "cda fájlformátum specifikációja"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ a CDA fájlformátumról és az API-król, amelyek CDA-fájlokat hozhatnak létre, konvertálhatnak és megnyithatnak.",
  "title" :"CDA - CD Audio Track parancsikon fájl",
  "linktitle" : "CDA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## Mi az a CDA fájl?

A .cda kiterjesztésű fájl egy kis csonkfájl, amelyet a Microsoft Windows hoz létre az audio CD-n lévő minden egyes hangsávhoz. Ezek a fájlok tipikus információkat tartalmaznak, például a műsorszámok idejét és egy Windows parancsikont, amely lehetővé teszi a felhasználók számára az adott hangsávok elérését. A CDA-fájlok nem zenék, hanem a tárolón valahol létező zenei fájlra mutatnak. Mondhatjuk egy CD-n található hangfájl parancsikonjaként.

## CDA fájlformátum

A CDA fájlformátum arra szolgál, hogy megmondja a számítógépnek, hogy melyik hangfájlt kell lejátszani a CD-n. Így a CDA-fájlok használhatatlanná válnak, ha elválasztják az általuk képviselt CD-től. A CDA-fájlokat általában RIFF-forrásoknak tekintik. A .cda fájl jelenlegi verziójában csak egy „CDDA” nevű darab található, és csak egy „FMT” nevű adatblokkot tartalmaz. Ez a blokk 24 bájt hosszú. A Windows által létrehozott azonosítót a Windows 95 és Windows 98 rendszerhez kapcsolódó CD-meghajtó használja, és a lejátszója nem tud csatlakozni a FreeDB-hez vagy a CDDB-hez. Annak érdekében, hogy megjelenítse a dal címét és az előadó nevét, ezt az információt kézzel kell beírnia a cdplayer.ini fájlba.

### CDA-fájl szervezése

Az alábbi táblázat a tipikus eltolásokkal kapcsolatos információkat tartalmazza:
| offset | hossza | tartalom |
---|---|---|
| 0x00 | 4 | a 4 ASCII karakter "RIFF" |
| 0x04 | 4 | a következő darab mérete: mindig 36 (44 - 8), 4 bájton (Intel sorrendben) |
| 0x08 | 4 | csonk azonosító: a 4 ASCII karakter "CDDA" |
| 0x0C | 4 | a 3 "fmt" ASCII-karakter, majd egy szóköz |
| 0x10 | 4 | a darab hossza: mindig 24, 4 bájton (Intel sorrendben) |
| 0x14 | 2 | a CD formátum verziója, 2 bájton (Intel rendelés). 2006 májusában mindig egyenlő 1-gyel. |
| 0x016 | 2 | a tartomány száma, 2 bájton (Intel sorrendben). Az első szám 1-es. |
| 0x18 | 4 | a Windows által a cdplayer.exe számára kiszámított azonosító. |
| 0x1c | 4 | tartomány eltolás, képkockák számában (Intel sorrendben) |
| 0x20 | 4 | a pálya időtartama, a képkockák teljes száma (Intel sorrendben) |
| 0x24 | 1 | tartomány helyzete: keretek |
| 0x25 | 1 | hatótávolság: másodperc |
| 0x26 | 1 | hatótávolság: perc |
| 0x27 | 1 | egy null byte (bináris érték 0) |
| 0x28 | 1 | a pálya időtartama: keretek |
| 0x29 | 1 | a pálya időtartama: másodperc |
| 0x2a | 1 | a pálya időtartama: perc |
| 0x2b | 1 | egy null byte (bináris érték 0) |

## Hivatkozások

* [.cda fájl – a Wikipédia által](https://en.wikipedia.org/wiki/.cda_file)

