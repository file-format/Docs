{
  "date" : "2021-08-17",
  "keywords" :[ "udf fájl", "udf fájl formátum", "mi az udf fájl", "fájl", "udf példa", "udf fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"További információ az UDF fájlformátumról és az API-król, amelyek UDF-fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"UDF - univerzális lemezformátum fájl",
  "linktitle" : "UDF",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-17"
}

## Mi az UDF fájl?
Az .udf kiterjesztésű fájl egy lemezképformátum, amelyet általában fájlok optikai adathordozóra való mentésére használnak; használható DVD-k, CD-k és egyéb optikai adathordozók írására; fájlok gyűjteményét tárolja az UDF szabványban meghatározott könyvtárstruktúra használatával; lehetővé teszi a fájlok törlését és módosítását a céllemezen, még azok írása után is. Az Optical Storage Technology Association szabványként állította be az UDF fájlrendszert, hogy közös fájlrendszert képezzen az összes optikai adathordozóhoz, például az újraírható optikai adathordozókhoz és az írásvédett adathordozókhoz.

## UDF fájlformátum
Az UDF fájlformátum egy nyílt, gyártó-semleges fájlrendszer számítógépes adattároláshoz sokféle média számára. Általában DVD-khez és újabb optikai lemezformátumokhoz használták. A szoftver általában kötegelt folyamatban kezeli az UDF fájlrendszert, és egyetlen lépésben kiírja optikai adathordozóra. Amikor azonban csomagokat ír újraírható adathordozóra, az UDF lehetővé teszi a fájlok létrehozását, törlését és módosítását a lemezen, hasonlóan egy általános célú fájlrendszerhez, amelyet cserélhető adathordozókon, például flash meghajtókon vagy hajlékonylemezeken tenne.
### UDF specifikációk
Az UDF szabvány a következő három fájlrendszer-változatot határozza meg:

- **Sima felépítés**: Ez az eredeti formátum, amelyet minden UDF-változat támogat. A szabvány első verziójában vezették be, ez a formátum bármilyen típusú lemezen használható, amely véletlenszerű olvasási vagy írási hozzáférést tesz lehetővé, mint például a DVD+RW, merevlemezek és DVD-RAM adathordozók.
- **ÁFA build**: Kifejezetten egyszer írható adathordozóra való íráshoz használatos. Az áfa egy kiegészítő szerkezet a lemezen, amely lehetővé teszi a csomagírást; vagyis a fizikai blokkok újraleképezése a lemezen lévő fájlok vagy egyéb adatok módosítása vagy törlése esetén. Az egyszer írható adathordozók esetében a teljes lemez virtualizálva van, így az egyszer írható jelleg átláthatóvá válik a felhasználó számára; a lemez ugyanúgy kezelhető, mint egy újraírható lemez.
- **Spared (RW) build**: Kifejezetten újraírható adathordozóra való íráshoz használatos. Hozzáad egy extra takarékossági táblázatot, hogy kezelje azokat a hibákat, amelyek végül előfordulnak a lemez többször átírt részein. Ez a táblázat elmenti az elhasználódott szektorok nyomvonalát, és újra leképezi azokat működő szektorokra. Az UDF hibakezelése nem vonatkozik azokra a rendszerekre, amelyek már megvalósítanak egy másik hibakezelési formát, például a Mount Rainier-t (MRW) optikai lemezekhez vagy lemezvezérlőt merevlemezekhez.
 




## Hivatkozások


* [Windows Imaging Format – a Wikipedia által](https://en.wikipedia.org/wiki/Windows_Imaging_Format)


