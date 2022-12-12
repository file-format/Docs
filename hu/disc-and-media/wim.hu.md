{
  "date" : "2021-08-11",
  "keywords" :[ "wim fájl", "wim fájl formátum", "mi az a wim fájl", "fájl", "wim példa", "wim fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"További információ a WIM fájlformátumról és az API-król, amelyek WIM-fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"WIM - Windows Imaging Format File",
  "linktitle" : "WIM",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-11"
}

## Mi az a WIM fájl?
A .wim kiterjesztésű fájlok először a Windows Vista rendszerben jelentek meg. A WIM egy fájl alapú képalkotási formátumhoz tartozik, amelyet általában a Microsoft Windows Vista rendszerben vezettek be. Lehetővé teszi egyetlen lemezkép telepítését különböző számítógépes platformokon. A WIM-fájlok a fájlok, például a frissítések, illesztőprogramok és összetevők kezelésére használhatók az operációs rendszer lemezképének újraindítása nélkül. Az AQ WIM fájl egy sor fájlt és kapcsolódó metaadatokat tartalmaz, amelyek nagyon hasonlítanak más lemezfájlformátumokhoz.

## WIM fájlformátumok
A WIM fájlformátum nem olyan, mint a szektoralapú formátumok, például a VHD vagy az IS, valójában fájlalapú, ami azt jelenti, hogy a WIM információinak alapvető egysége egy fájl. A fájlalapúság alapvető előnye, hogy a fájl egyetlen példányban történő tárolása többször hivatkozik a fájlrendszer fában és a hardverfüggetlenség. Csökkenti a különböző fájlok külön-külön történő megnyitásának és bezárásának többletköltségét, mivel a fájlok egyetlen WIM-en belül vannak tárolva. fájlt. A WIM-fájlok több lemezképet is tárolhatnak, amelyekre egyedi nevük vagy numerikus indexük hivatkozik.
### Tömörítési algoritmusok támogatása
A WIM a következő tömörítési algoritmuscsaládokat támogatja csökkenő sebességben és növekvő arányban:
- XPRESS
- LZX
- LZMS
- Szilárd tömörítés.
Az első három család LZ77 alapú, míg a Solid-compression az LZMS-sel együtt került bevezetésre a WIMGAPI Windows 8 és a DISM Windows 8.1 rendszerben.
### Eszközök a WIM fájlformátumhoz
A következő eszközök általában támogatják a WIM fájlformátumot:

- **ImageX**: Parancssori eszköz a Windows lemezképek szerkesztésére, létrehozására és telepítésére a Windows képformátumban. A vonatkozó WIMGAPI-val együtt az ingyenes Windows automatizált telepítőkészlet részeként kerül terjesztésre. A Windows Vista rendszertől kezdve a Windows Telepítő a WAIK API-t használja a Windows telepítéséhez.
- **DISM**: A Windows 7 és a Windows Server 2008 R2 rendszerben bevezetett eszköz, amely szolgáltatással kapcsolatos feladatokat tud végrehajtani egy Windows telepítőlemezen, legyen az online kép vagy offline kép egy mappában vagy WIM-fájlban. ez az eszköz képes volt képek be- és lecsatolására, eszközillesztő hozzáadására egy offline képhez, valamint a telepített eszközillesztők lekérdezésére egy offline képben.
 




## Hivatkozások


* [Windows Imaging Format – a Wikipedia által](https://en.wikipedia.org/wiki/Windows_Imaging_Format)


