{
  "date" : "2023-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LAS - Lidar LASer fájlformátum",
  "description":"További információ a LAS fájlformátumról és az API-król, amelyek LAS-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "LAS",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2023-07-18"
}

## Mi az a LAS fájl?

A LAS (Lidar LASer) fájlformátum egy bináris fájlformátum, amelyet kifejezetten a lidar pontfelhő adatok tárolására terveztek. Az Amerikai Fotogrammetriai és Távérzékelési Társaság (ASPRS) fejlesztette ki és tartja karban, mint a lidar adatcsere és interoperabilitás szabványosított formátumát.

A LAS fájlok részletes információkat tárolnak az egyes lidar pontokról, beleértve azok 3D koordinátáit (x, y és z), intenzitásértékeket, osztályozási kódokat és további attribútumokat. A formátum támogatja a diszkrét visszatérést és a teljes hullámforma lidar adatokat is, lehetővé téve a lézerimpulzusonkénti többszörös visszatérések tárolását.

## LAS fájlformátum

A LAS fájl szerkezete három fő részből áll: a fájl fejlécéből, a változó hosszúságú rekordokból (VLR) és a pont adatrekordokból.

1. Fájlfejléc: A fájlfejléc alapvető információkat tartalmaz a LAS-fájlról, például az adatformátum verzióját, a pontadatok formátumát, a pontok számát, a határolókeret koordinátáit, a koordináta-referenciarendszert (CRS) és egyéb metaadatokat. Összefoglalja a fájlban található lidar-adatokat.

2. Változó hosszúságú rekordok (VLR): A VLR-ek nem kötelezőek, és további metaadatokat és egyéni információkat tárolhatnak a lidar adatokról. A VLR-ek rugalmasságot tesznek lehetővé a formátum kiterjesztésében, hogy megfeleljenek az egyedi felhasználói igényeknek. A VLR-ekre példák az érzékelőrendszerre vonatkozó információk, az adatfeldolgozási paraméterek vagy az osztályozási sémák.

3. Pont adatrekordok: A pont adatrekordok tárolják a tényleges lidar méréseket. Minden pontadatrekord egyetlen lidar pontot képvisel, és olyan attribútumokat tartalmaz, mint az x, y és z koordináták, intenzitásértékek, osztályozási kódok (pl. talaj, növényzet, épületek) és egyéb, felhasználó által meghatározott attribútumok. A pontrekordok időbélyegeket, visszatérési számokat és szkennelési szögeket is tárolhatnak.

A LAS-fájlok különböző adatformátumokat támogatnak (0-tól 10-ig), hogy a különféle típusú lidar-adatokhoz és a szükséges információszinthez illeszkedjenek. Például a 0 formátum egy egyszerű pontformátumot jelent alapvető információkkal, míg az 1–3 formátumok átfogóbb adatokat biztosítanak, beleértve a hullámforma információkat is minden visszatéréshez.

A LAS fájlokat széles körben támogatják a lidar szoftverek és feldolgozó eszközök, így a lidar adatcsere és -elemzés szabványos formátuma. Ezenkívül a LAS fájlok veszteségmentes tömörítési technikákkal tömöríthetők a fájlméret csökkentése érdekében, miközben megőrizzük az eredeti adathűséget. A LAS-fájlok tömörített verzióját gyakran LAZ-nak nevezik, amely hatékony tárolási és adatátviteli lehetőségeket kínál.

## Hivatkozások

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
