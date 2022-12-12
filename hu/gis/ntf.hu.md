{
  "date" : "2021-07-28",
  "keywords" :[ "ntf fájl", "ntf fájl formátum", "mi az ntf fájl", "fájl", "ntf példa", "ntf fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NTF - Nemzeti átviteli formátumú fájlok",
  "description":"További információ az NTF fájlformátumról és az NTF-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "NTF",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-28"
}

## Mi az NTF fájl?
Az .ntf kiterjesztésű fájlokat **National Transfer Format (NTF)** fájloknak nevezzük; többnyire a UK Ordnance Survey (OS) használja; kifejezetten térinformatikai adatok továbbítására. A brit szabványügyi intézet kezeli. Ez lett az Ordnance Survey digitális adatok szabványos átviteli formátuma. Az Egyesült Királyság National Grid vetülete, amely a Transverse Mercator egyik típusa, tartalmazza az NTF-fájlok minden georeferált információt.

## NTF fájlformátum
Az NTF fájlformátum az Ordnance Survey tulajdona az Egyesült Királyságban; a GDB könyvtár támogatja az importálást. Az NTF fájlformátum jelenlegi verziója 2.0. Ezt a fájlformátumot azért vezették be, hogy a **PCIDSK** vektorszegmens korlátozását kezelje, amely struktúránként csak egy attribútummezőt tartalmaz, de számos attribútum is kivonható vektoradatokkal. Az NTF fájlformátum két szegmensből áll. Minden szegmens ugyanazokból a vektorokból áll, de különböző attribútumokkal. Az NTF vektorfájl első szegmense tartalmazza azokat a vektorokat, amelyek attribútumaként a jellemző kódszámot tartalmazzák. A második szegmens azokat a vektorokat tartalmazza, amelyek attribútuma az érték.

### Koordináta-hivatkozási rendszer
A GDB könyvtár raszteres és vektoros adatokat reprezentál a megfelelő TM vetületi jellemzőkkel:

- Referencia hosszúság: 49,0
- Referencia szélesség: 2.0
- Hamis húsvét: 400 000
- Hamis észak: -100 000
- Skála: 0,9996012717
- Ellipszoid: Airy 1830 (E009)
Nem áll rendelkezésre támogatás az NTF-fájlok frissítéséhez vagy írásához, és a DTM-fájlokhoz sem lehet hivatkozni.

### Ogrinfo példa
A következő példa az **ogrinfo**-t használja egy NTF-fájlban a rétegszámok lekéréséhez:
```
> ogrinfo llcontours.ntf
    INFO: Open of 'llcontours.ntf'
    using driver 'UK .NTF' successful.
    1: LANDLINE_POINT (Point)
    2: LANDLINE_LINE (Line String)
    3: LANDLINE_NAME (Point)
    4: FEATURE_CLASSES (None)
```




## Hivatkozások

* [Az Egyesült Királyság nemzeti átutalási formátuma (NTF)](https://catalyst.earth/catalyst-system-files/help/references/gdb_r/gdb3N292.html)
* [Web Mapping – Illustrated by Tyler Mitchell](https://www.oreilly.com/library/view/web-mapping-illustrated/0596008651/re15.html)

