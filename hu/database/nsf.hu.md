{
  "date" : "2020-11-11",
  "keywords" :[ "NSF", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ az NSF fájlformátumról és az NSF-fájlok létrehozására és megnyitására alkalmas API-król.",
  "title" :"NSF fájlformátum - Lotus Notes adatbázis formátum",
  "linktitle" : "NSF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Mi az NSF fájl?

Az .nsf (Notes Storage Facility) kiterjesztésű fájl az [IBM Notes szoftver](https://en.wikipedia.org/wiki/HCL_Domino) által használt adatbázis-fájlformátum, amely korábban Lotus Notes néven volt ismert. Meghatározza a sémát különböző típusú objektumok, például e-mailek, találkozók, dokumentumok, űrlapok és nézetek tárolására. Mindezek az információk egyetlen NSF-fájlban találhatók az üzleti együttműködéshez, hasonlóan a PST/OST-fájlhoz. Az NSF-fájlokat megnyitni képes alkalmazások közé tartozik az IBM Lotus Notes és az IBM Domino.

## Az NSF fájlformátum specifikációi

Az NSF-fájlok bináris jellegűek, és specifikációikat Joachim Metz a [Github] webhelyen (https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database% 20file%20format.asciidoc). Az alábbiak szerint egy NSF-fájl a következőket tartalmazza:

* Fájl fejléc
* Adatbázis fejléc

Ezen kívül a következőkből áll:

* Superblock
* Vödör leíró blokk
* Bitmap
* Record Relocation Vector vödör
* Összefoglaló vödrök
* Nem összefoglaló kockák


### NSF fájl fejléc

Az NSF fájl fejléce 6 bájt méretű. A következőkből áll:

|Eltolás|Méret|Érték|Leírás|
---|---|---|---|
0|2|0x1a 0x00|Aláírás|
2|4| |Az adatbázis fejléc mérete|

### Adatbázis fejléce

Az NSD Database fejléce a következő megerősített értékeket tartalmazza.

* Adatbázis információk
* Adatbázis azonosító (DBID)
* Replikációs információk
* Adatbázis információs puffer jelzők
* Cím
* Kategóriák
* Osztály
* Tervezési osztály (sablon neve)
* Különleges megjegyzés azonosítók
* Bélés
* Adatbázis információ 2
* Adatbázis információk 3
* Adatbázis információ 4
* Adatbázis információ 5
* Bélés
* Adatbázis-példányazonosító (DBIID)
* Replikációs előzmények

## Hivatkozások

* [NSF-formátum – Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc)

