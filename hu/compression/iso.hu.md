{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ISO - Lemezképfájl formátum",
  "description":"Mi az az ISO-fájl és API-k, amelyek képesek ISO-fájlok létrehozására és megnyitására.",
  "linktitle" : "ISO",
  "menu" : {
    "docs" : {
     "identifier": "compression-iso",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Mi az ISO fájl?

Az .iso kiterjesztésű fájl egy tömörítetlen archív lemezképfájl, amely egy optikai lemezen, például CD-n vagy DVD-n lévő teljes adat tartalmát reprezentálja. Az [ISO-9660](https://www.iso.org/standard/17505.html) szabvány alapján az ISO képfájlformátum tartalmazza a lemez adatait a benne tárolt fájlrendszer információival együtt. Az ISO-fájlok azon képessége, hogy a tartalom pontos másolatát tartalmazzák, tökéletes fájltípussá teszi a CD-k/DVD-k másolatainak készítéséhez, és többnyire rendszerindító adatok tárolására használják telepítéshez. Legtöbbször az ISO-fájlok USB-re/CD-re/DVD-re vannak írva rendszerindító tartalomként a gép indításához a telepítéshez. Az ISO-fájlok MIME típusú application/x-iso9660-image típusúak.

## ISO fájlformátum

Az ISO-fájlformátum nem hasonlít a többi konténerfájl-formátumhoz, bár archiválja az adatok meghatározott tartalmát. Az archívum bináris fájlként jön létre, a tartalom és a fájlrendszer információinak pontos szerkezetével. Az ISO-fájlformátumot az [ISO-9660](https://en.wikipedia.org/wiki/ISO_9660) írja le az alábbiak szerint.

### Az ISO fájl legfelső szintű szerkezete

A fájl általános szerkezete a következőkből áll:

* "Rendszerterület" - 32 768 bájt, és az ISO_9660 nem használja
* "Adatterület" - Kötetleíró készletből és elérési út táblákból, könyvtárakból és fájlokból áll

### Kötetleíró készlet

Az adatterület a kötetleírókészlettel kezdődik, amely egy vagy több kötetleíró halmaza, amely egy kötetleírókészlet-lezáróval végződik. Ezek együttesen fejlécként működnek az adatterület számára, leírva annak tartalmát (hasonlóan a FAT, HPFS és NTFS formátumú lemezek által használt BIOS paraméterblokkhoz).

A kötetleíró készlet az alábbiak szerint látható.

|Kötet leíró készlet|
---|
|Kötet leíró #1|
|...|
|Térfogatleíró #N|
|Kötet leírókészlet lezáró|

#### Kötetleíró

Minden kötetleíró 2048 bájt méretű, és a következő szerkezettel rendelkezik:

|Rész |Típus |Azonosító |Verzió |Adatok|
---|---|---|---|---|
|Méret |1 bájt |5 bájt (mindig 'CD001') |1 bájt (mindig 0x01) |2041 bájt|

## Hivatkozások

* [Optikai lemez képe – Wikipédia](https://en.wikipedia.org/wiki/Optical_disc_image)
* [Fájl aláírások](https://www.garykessler.net/library/file_sigs.html)
* [ISO 9660 – Wikipédia](https://en.wikipedia.org/wiki/ISO_9660)

