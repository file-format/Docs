{
  "date" : "2023-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LAZ - tömörített LIDAR adatcsere fájl",
  "description":"További információ a LAZ fájlformátumról és az API-król, amelyek LAZ fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "LAZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2023-07-18"
}

## Mi az a LAZ fájl?

A LAZ fájlformátum a LAS (Lidar LASer) fájlformátum tömörített változata, amelyet kifejezetten a lidar pontfelhő adatok tárolására terveztek. A LAZ-fájlok megőrzik ugyanazokat az adatokat és szerkezetet, mint a LAS-fájlok, de veszteségmentes tömörítési technikákat alkalmaznak a fájlméret csökkentése érdekében, miközben megőrzik az eredeti adathűséget.

## LAZ fájlformátum – rövid előzmények

A LAZ fájlformátumot azért fejlesztették ki, hogy kielégítse a nagyméretű lidar adatkészletek hatékony tárolása és továbbítása iránti növekvő igényt. A LAS fájlok tömörítésével a LAZ fájlok jelentősen csökkentik a méretüket, így könnyebben kezelhetők és átvihetők. A tömörítést különböző algoritmusok, például entrópiakódolás és változó hosszúságú kódolás kombinációjának alkalmazásával érik el, hogy a lidar-pont attribútumokat kompaktabb formában jelenítsék meg.

## LAZ fájlformátum

A tömörítés ellenére a LAZ-fájlok továbbra is képesek az eredeti LAS-adatok teljes visszaállítására információvesztés nélkül. Ez azt jelenti, hogy a LAZ-fájl kicsomagolása után ugyanúgy feldolgozható és elemezhető, mint egy tömörítetlen LAS-fájl. A tömörítési és kitömörítési folyamat általában speciális szoftverrel vagy olyan könyvtárakkal történik, amelyek támogatják a LAZ formátumot.

A LAZ fájlformátum fenntartja a kompatibilitást a LAS fájlokkal, biztosítva a lidar szoftverek és feldolgozóeszközök közötti együttműködést. Ez azt jelenti, hogy az olyan alkalmazások, amelyek képesek olvasni és feldolgozni a LAS-fájlokat, általában minden módosítás nélkül képesek kezelni a LAZ-fájlokat. Ezenkívül a LAZ-fájlok továbbra is tartalmazzák a fájlfejlécet, a változó hosszúságú rekordokat (VLR-eket) és a pontadatrekordokat, megőrizve ugyanazt a szerkezetet, mint a LAS-fájlok.

## A LAZ fájlformátum előnyei

**Csökkentett fájlméret:** A LAZ-tömörítés jelentősen csökkenti a Lidar-adatkészletek fájlméretét, így könnyebben kezelhetővé, valamint könnyebben tárolhatóvá és továbbíthatóvá válik.

**Adatintegritás:** A LAZ-tömörítés veszteségmentes, ami azt jelenti, hogy a kitömörített adatok az eredeti LAS-adatok pontos másolata, így nincs információvesztés vagy pontosság.

**Interoperabilitás:** A LAZ fájlok kompatibilisek a LAS fájlokkal, lehetővé téve a zökkenőmentes integrációt a meglévő lidar szoftverekkel és munkafolyamatokkal.

**Hatékony feldolgozás:** Csökkentett méretüknek köszönhetően a LAZ-fájlok gyorsabban betölthetők és feldolgozhatók, javítva a teljes feldolgozási és elemzési időt.

A LAZ fájlformátum széles körben elterjedt a lidar közösségben a tömörített lidar adattárolás és -csere szabványaként. Egyensúlyt kínál a hatékony adattömörítés és az adatintegritás között, lehetővé téve a nagy lidar adatkészletek egyszerűbb kezelését, miközben megőrzi az eredeti adatok pontosságát és minőségét.

## Hivatkozások

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
