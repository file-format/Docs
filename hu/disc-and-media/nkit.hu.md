{
  "date" : "2022-04-01",
  "keywords" :[ "nkit fájl", "nkit fájlformátum", "mi az nkit fájl", "fájl", "nkit példa", "nkit fájl kiterjesztése", "kiterjesztés", "formátum", "nkit lábléc", "fájl nkit formátuma"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"További információ az NKIT fájlformátumról és az API-król, amelyek NKIT fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"NKIT - Lemezképfájl formátum",
  "linktitle" : "NKIT",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-04-01"
}

## Mi az a NKIT fájl?

Az NKIT fájl a NintendoWii és GameCube játékokból kinyert adatok lemezképe. Az NKIT a Nintendo Toolkit formátumhoz készült. Az eredményül kapott tömörítési [ISO](/hu/compression/iso/) fájl e játékok főbb adatait használja fel olyan emulátorprogramokkal való futtatáshoz, mint a Dolphin, a Swiss és a Nintendont. Az NKit nyers (iso) és tömörített (gcz) fájlformátumokban érkezik, amelyeket úgy terveztek, hogy a lejátszási képességet és a méretet megtartsák.

## NKIT fájlformátum

Az NKit fájlformátum nem veszteséges formátum, és a Nintendo Wii és GameCube képek zsugorítására és visszaállítására szolgál. A formátumok ISO és GCZ fájlformátumban érhetők el minden GameCube és Wii játékhoz.

|Rendszer |Formátum |Hardver támogatott |Dolphin támogatott |Visszaállítható 1:1 |Megjegyzések|
---|---|---|---|---|---|
|GameCube| nkit.iso| Igen |Igen| Igen |Ugyanaz, mint a tömörített GameCube iso|
|GameCube| nkit.gcz| Nem| Igen| Igen |A GCZ a Dolphin saját blokkkereshető tömörítési formátuma|
|Wii| nkit.iso| Nem Igen| Igen| Az RVT-H formátum csak a Dolphin|-ban játszható le
|Wii| nkit.gcz| Nem Igen| Igen| Az RVT-H GCZ-ben csak Dolphinban játszható|

### NKIT fejléc

Az NKIT fájlformátum fejléce a következő.

|Eltolás |Hosszú |Név|
---|---|---|
|0x200 |0x4 |NKit fejléc 'NKIT'|
|0x204 |0x4 |NKit verzió ' v01'|
|0x208 |0x4 |Forráskép eredeti CRC32|
|0x20C |0x4 |NKit CRC – a CRC32 NKit-fájlt egyenlővé teszi a forrás CRC-vel 0x208-nál (0x4-nél a GCZ-ben)|
|0x210 |0x4 |Forráskép hossza|
|0x214 |0x4 |Kényszerített szemétazonosító (ha a lemezazonosító eltér – ritka – csak GameCube)|
|0x218 |0x4 |Wii Frissítse a CRC32 partíciót, ha eltávolítja a konvertálás során|

## Hivatkozások ##

* [NKIT fájlformátum – gbatemp](https://wiki.gbatemp.net/wiki/NKit/NKitFormat)

