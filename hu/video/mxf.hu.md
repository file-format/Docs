{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MXF - Anyagcsere formátum",
  "keywords" :[ "MXF", "matroska video", "mkv format", "how to play MXF files", "SMPTE", "multimedia", "video" ],
  "description":"További információ az MXF fájlformátumról és az API-król, amelyek MXF fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "MXF",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-01"
}

## Mi az MXF fájl?

Az .mxf kiterjesztésű fájl egy multimédiás tárolóformátum, amely digitális video- és audiomédiát tartalmaz a fájl metaadataival együtt. Az SMPTE (Society of Motion Picture and Television Engineers) szabványt követi, amely a mérnökök, a technológia, valamint a média- és szórakoztatóiparban dolgozó szakemberek globális szövetsége. Az MXF-fájlok más fájlformátumokká konvertálhatók, például [AVI](/hu/video/avi/) vagy [MOV](/hu/video/mov/).

## MXF fájlformátum

Az MXF fájlok valójában bináris fájlok, amelyek meghatározott formátumú bájtok sorozatából állnak. A dekódoló alkalmazásoknak meg kell felelniük ennek a formátumnak ahhoz, hogy megértsék azt, és információkat nyerjenek ki belőle. A formátum lehetővé teszi új elemek hozzáadását a visszafelé kompatibilitás megszakítása nélkül az alábbiakban ismertetett KLV kódolás használatával.

* Kulcs – az elem azonosítója, egy SMPTE Universal Label (UL)
* Hossz – az adat hossza, amely a változó hosszúságú kódolás, amelyet az elemhez szükséges hely csökkentése érdekében használnak
* Érték – az elem tényleges értéke.

### SMPTE formátum specifikációi

Az MXF fájlformátumot a következő SMPTE specifikációk határozták meg.

* SMPTE ST 377-1:2011. Televízió — Anyagcsere formátum (MXF) — Fájlformátum specifikáció
* SMPTE ST 377-2 (2012 januárjától folyamatban lévő munka). KLV kódolt kiterjesztési szintaxis az MXF-hez.
* SMPTE ST 378:2004 (Archiválva 2010). Televízió – Anyagcsere-formátum (MXF) – 1a. működési minta (egy tétel, egy csomag)
* SMPTE ST 379-1:2009. Anyagcsere formátum (MXF) – MXF általános tároló
* SMPTE ST 379-2:2010. Anyagcsere formátum (MXF) -- MXF korlátozott általános tároló
* SMPTE ST 380:2004. Televízió – Anyagcsere-formátum (MXF) – Leíró metaadat-séma-1 (standard, dinamikus)
* SMPTE ST 381-1:2005. Televízió – Anyagcsere formátum (MXF) – MPEG adatfolyamok hozzárendelése az MXF általános tárolóba (dinamikus)
* SMPTE ST 381-2:2011. Anyagcsere formátum (MXF) – MPEG adatfolyamok hozzárendelése az MXF korlátozott általános tárolóhoz
* SMPTE ST 382:2007. Anyagcsere formátum (MXF) – AES3 adatfolyamok és Broadcast Wave Audio hozzárendelése az MXF általános tárolóhoz
* SMPTE ST 383:2008. Televízió – Anyagcsere formátum (MXF) – DV-DIF adatok hozzárendelése az MXF általános tárolóhoz
* SMPTE ST 384:2005. Televízió – Anyagcsere formátum (MXF) – Tömörítetlen képek hozzárendelése az MXF általános tárolóba
* SMPTE ST 385:2004. Televízió – Anyagcsere-formátum (MXF) – Az SDTI-CP Essence és a metaadatok hozzárendelése az MXF általános tárolóba
* SMPTE ST 386:2004 (Archiválva 2010). Televízió – Anyagcsere formátum (MXF) – D-10 típusú essence adatok hozzárendelése az MXF általános tárolóhoz
* SMPTE ST 387:2004 (Archiválva 2010). Televízió – Anyagcsere formátum (MXF) – D-11 típusú essence adatok hozzárendelése az MXF általános tárolóhoz
* SMPTE ST 388:2004 (Archiválva 2010). Televízió – Anyagcsere formátum (MXF) – A törvény által kódolt hang hozzárendelése az MXF általános tárolóhoz
* SMPTE ST 389:2005. Televízió — Anyagcsere formátum (MXF) — MXF általános konténer fordított lejátszási rendszerelem
* SMPTE ST 390:2011. Televízió – Anyagcsere-formátum (MXF) – „Atom” speciális működési minta (egyetlen elem egyszerűsített ábrázolása)
* SMPTE ST 391:2004 (Archiválva 2010). Televízió – Anyagcsere-formátum (MXF) – 1b. működési minta (egy tétel, csoportos csomagok)
* SMPTE ST 392:2004. Televízió – Anyagcsere-formátum (MXF) – 2a. működési minta (lejátszási lista elemek, egy csomag)
* SMPTE ST 393:2004. Televízió – Anyagcsere formátum (MXF) – 2b működési minta (lejátszási lista elemek, csoportos csomagok)
* SMPTE ST 394:2006. Televízió – Anyagcsere-formátum (MXF) – 1. rendszerséma az MXF általános tárolóhoz
* SMPTE ST 405:2006. Televízió – Anyagcsere-formátum (MXF) – Elemek és egyedi adatelemek az MXF általános konténerrendszerhez 1. séma
* SMPTE ST 407:2006. Televízió – MXF – 3a és 3b működési minták
* SMPTE ST 408:2006. Televízió – MXF – 1c, 2c és 3c működési minták
* SMPTE ST 410: 2008. Anyagcsere formátum - Általános adatfolyam-partíció.
* SMPTE ST 422:2006. Anyagcsere formátum – JPEG2000 kódfolyamok hozzárendelése az MXF általános tárolóba
* SMPTE ST 429.4:2006. D-Cinema csomagolás – MXF JPEG 2000 alkalmazás
* SMPTE ST 429.5:2006. D-Cinema Packaging — Időzített szövegsáv fájl
* SMPTE ST 429.6:2006. D-Cinema Packaging – MXF Track File Essence titkosítás
* SMPTE ST 434:2006. Anyagcsere-formátum – XML-kódolás a metaadatokhoz és a fájlszerkezeti információkhoz
* SMPTE ST 436:2006. Televízió – MXF-leképezések VBI-vonalakhoz és kiegészítő adatcsomagokhoz
* SMPTE ST 2019-4:2009. VC-3 kódolási egységek hozzárendelése az MXF általános tárolóba
* SMPTE ST 2037:2009. A VC-1 hozzárendelése az MXF általános tárolóhoz
* SMPTE RP 2008:2008. Anyagcsere-formátum – AVC-folyamok hozzárendelése az MXF általános tárolóba
* SMPTE RP 2057:2011. Szövegalapú metaadat-átvitel MXF-ben
* SMPTE EG 41:2004. Anyagcsere-formátum (MXF) – Műszaki útmutató. Megjegyzés: Ez a dokumentum 2012 januárjában már nem szerepelt az SMPTE webhelyén.
* SMPTE EG 42:2004. Anyagcsere-formátum (MXF) – MXF leíró metaadatok
* SMPTE RDD 3:2008. e-VTR MXF interoperabilitási specifikáció
* SMPTE RDD 9-2009. A Sony MPEG Long GOP termékek MXF együttműködési specifikációi
* SMPTE metaadat-nyilvántartási táblázatkezelő menü.

### MXF strukturális metaadatok

A strukturális metaadatok alapvetőek az MXF-fájlokban, mivel hasznos információkat tartalmaznak a fájl tartalmáról. Az MXF metaadatok olyan információkat tartalmaznak, mint a képkockasebesség, a keretméret, a fájl létrehozásának dátuma és az egyéni módosítás dátuma. A szerkezeti metaadatok egy MXF-fájl szerkezetét és képességeit írják le, amelyek magukban foglalják a különböző alapvető összetevők technikai leírását és a kimeneti idővonal összeállításának közvetítését.

## Hivatkozások

* [MXF - Wikipedia](https://en.wikipedia.org/wiki/Material_Exchange_Format)
* [MXF – Előrehaladási jelentés](http://tech.ebu.ch/docs/techreview/trev_2010-Q3_MXF-1.pdf)
* [OpenSource C++ Library for MXF](http://www.freemxf.org/)

