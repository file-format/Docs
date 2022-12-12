{
  "date" : "2019-10-11",
  "keywords" :[ "gz fájl", "gz fájl formátum", "mi az a gz fájl", "fájl", "gz példa", "gz fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GZ fájlformátum - GNU tömörített archív fájl",
  "description":"További információ arról, hogy mi az a GZ-fájl és az API-k, amelyek GZ-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "GZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a GZ fájl?

A GZ-fájl egy tömörített archívum, amely a szabványos [gzip](https://en.wikipedia.org/wiki/Gzip) (GNU zip) tömörítési algoritmussal jön létre. Több tömörített fájlt, könyvtárat és fájlcsonkot is tartalmazhat. Ezt a formátumot eredetileg a UNIX rendszereken használt tömörítési formátumok helyettesítésére fejlesztették ki. és még mindig az egyik leggyakoribb archívumtípus a Linux rendszereken. Az olyan alkalmazások, mint a [WinZip](https://www.winzip.com/en/), megnyithatják a GZ-fájlokat, hogy megtekintsék azok tartalmát Windows és MacOS rendszeren egyaránt.

## GZ fájlformátum - További információ

A Gzip a [DEFLATE](https://en.wikipedia.org/wiki/DEFLATE) algoritmust használja az archívum tömörítésére, és eltér a [ZIP](/hu/compression/zip/) archívumformátumtól abban, hogy a tömörítési algoritmust teljes archívumra alkalmazza. nem pedig az egyes fájlokat. Az Internet Engineering Task Force (IETF) által közzétett GZIP fájlformátum-specifikációk 4.3-as verziója részletes információkat tartalmaz a fájlformátumról. A fájlformátum a következőkből áll:

* Fájl fejléc
* Opcionális fejlécek
* Tömörített adatok
* Fájllábléc

## GZ fájl fejléc ##

A GZ fájl fejléce 10 bájtból áll, az alábbiak szerint:

|Eltolás|Méret|Érték|Leírás
---|---|---|---|
|0|2|0x1f 0x8b|Fájltípust azonosító mágikus szám
|2|1| |Tömörítési módszer * 0-7 (fenntartva) * 8 (leeresztés)
|3|1| |Fájljelzők
|4|4| |32 bites időbélyeg
|8|1| |Tömörítési zászlók
|9|1| |Operációs rendszerazonosító

### Fájljelzők ###

|Érték|Azonosító|Leírás
---|---|---|
|0x01|FTEXT|Ha be van állítva, a tömörítetlen adatokat szövegként kell kezelni bináris adatok helyett. Ez a jelző a többplatformos szövegfájlok sorvégi konverziójára utal, de nem kényszeríti ki.
|0x02|FHCRC|A fájl fejléc-ellenőrző összeget tartalmaz (CRC-16)
|0x04|FEXTRA|A fájl extra mezőket tartalmaz
|0x08|FNAME|A fájl eredeti fájlnév-karakterláncot tartalmaz
|0x10|FCOMMENT|A fájl megjegyzést tartalmaz
|0x20| |Fenntartva
|0x40| |Fenntartva
|0x80| |Fenntartva

### Operációs rendszer ###

|Érték|Leírás
---|---|
|0|FAT fájlrendszer (MS-DOS, OS/2, NT/Win32)
|1|Amiga
|2|VMS (vagy OpenVMS)
|3|Unix
|4|VM/CMS
|5|Atari TOS
|6|HPFS fájlrendszer (OS/2, NT)
|7|Macintosh
|8|Z-rendszer
|9|CP/M
|10|TOPS-20
|11|NTFS fájlrendszer (NT)
|12|QDOS
|13|Acorn RISCOS
|255|ismeretlen

## GZ opcionális fejlécek ##

Az opcionális extra fejlécek azok, amelyeket a fájljelzők jelölnek, és olyan információkat tartalmaznak, mint az eredeti fájlnév, extra mezők, megjegyzések és fejléc-ellenőrző összeg.

## Tömörített adatok ##

Ez a rész a DEFLATE tömörítési algoritmussal tömörített adatokat tartalmazza.

## GZ fájl lábléc ##

A fájl lábléce 8 bájt méretű, és a következő információkat tartalmazza.

|Eltolás|Méret|Leírás
---|---|---|
|0|4|Ellenőrző összeg (CRC-32)
|4|4|Tömörítetlen adatméret értéke bájtban

## Hivatkozások ##

* [gzip - Wikipédia](https://en.wikipedia.org/wiki/Gzip)
* [RFC1952: GZIP fájlformátum specifikáció] (http://tools.ietf.org/html/rfc1952), az IETF.

