{
  "date": "2023-01-10",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WOFF2 fájl – Web Open Font Format 2.0 fájl",
  "description": "Ismerje meg, mi az a WOFF2 fájl, valamint az API-k, amelyek létrehozhatnak és megnyithatnak WOFF2 fájlt.",
  "linktitle": "WOFF2",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-woff-hu2"
}
},
  "lastmod": "2023-01-10"
}

## Mi az a WOFF2 fájl?

A WOFF2 egy font fájlformátum, amely a Web Open Font Format (WOFF) tömörített változata. Úgy fejlesztették ki, hogy csökkentse a webes betűtípusok fájlméretét, lehetővé téve a gyorsabb betöltődést és a kisebb sávszélesség használatát. A WOFF2 a Brotli nevű tömörítési algoritmust használja a betűtípusadatok tömörítésére, ami a megfelelő [WOFF](/font/woff/) betűtípusoknál lényegesen kisebb fájlméreteket eredményezhet. Ezt a formátumot a legtöbb modern webböngésző támogatja, köztük a Chrome, a Firefox, a Safari, az Opera és az Edge (14-es verziótól).

## WOFF2 fájlformátum - További információ

A WOFF2 betűkészlet-fájl belső fájlstruktúrája több különböző részből áll, beleértve a fejlécet, a metaadatokat, a táblakönyvtárat és magát a fontadatokat.

 1. A fejléc információkat tartalmaz a fájl általános formátumáról, beleértve a verziószámot és a fájlban található táblázatok számát.

 1. A metaadatok szakasz olyan információkat tartalmaz, mint a betűtípus neve, szerzői joga és egyéb, a betűkészlettel kapcsolatos információk.

 1. A táblakönyvtár információkat tartalmaz a betűtípust alkotó különböző táblákról, beleértve azok helyét a fájlban és hosszukat.

 1. Maguk a betűtípusadatok több különböző táblázatra vannak osztva, amelyek mindegyike konkrét információkat tartalmaz a betűtípusról, például annak karaktereit és a hozzájuk tartozó karakterjeleket. Ezek a táblázatok a következőket tartalmazhatják:

 * A glyf” táblázat tartalmazza a tényleges betűtípus körvonalait, beleértve az egyes karakterek alakját és méretét.
 * A fej” táblázat általános információkat tartalmaz a betűtípusról, mint például a verziószám, a tervezési méret stb.
 * A hmtx” táblázat információkat tartalmaz a betűtípus mérőszámairól, beleértve a karakterek szélességét és helyzetét.
 * A kódolási folyamat befejezése után minden táblázatot tömörítünk és WOFF2 fájlformátumban tárolunk.

A szerkezet általánosságban úgy lett kialakítva, hogy lehetővé tegye a gyors elemzést és dekódolást, így a webböngészők gyorsan és hatékonyan tudják betölteni és megjeleníteni a betűtípust a webhelyen.

### WOFF2 fejléc
A WOFF fejléc egy azonosító aláírást tartalmaz, amely jelzi, hogy a fájl milyen típusú adatokat tartalmaz. A WOFF fejléc a mezőivel együtt a következő.

|Típus|Mezőnév|Leírás|
---|---|---|
|UInt32|aláírás |0x774F4632 'wOF2' |
|UInt32| flavor |A beviteli betűtípus sfnt verziója.|
|UInt32| hossz |A WOFF fájl teljes mérete.|
|UInt16| numTables |Bejegyzések száma a betűtípustáblázatok könyvtárában.|
|UInt16| fenntartva |Fenntartva; nullára állítva.|
|UInt32| totalSfntSize |A tömörítetlen betűtípusadatokhoz szükséges teljes méret, beleértve az sfnt fejlécet, a könyvtárat és a betűtípustáblázatokat (beleértve a kitöltést is).|
|UInt32| totalCompressedSize A tömörített adatblokk teljes hossza.|
|UInt16| majorVersion |A WOFF-fájl fő verziója.|
|UInt16| minorVersion |A WOFF fájl kisebb verziója.|
|UInt32| metaOffset |Eltolás a metaadatblokkhoz, a WOFF fájl elejétől.|
|UInt32| metaLength |Tömörített metaadatblokk hossza.|
|UInt32| metaOrigLength |A metaadatblokk tömörítetlen mérete.|
|UInt32| privOffset |Eltolás a privát adatblokkhoz, a WOFF fájl elejétől.|
|UInt32| privLength |Privát adatblokk hossza.|


## Hivatkozások
 * [w3 WOFF2 fájlformátum](https://www.w3.org/TR/WOFF2/)

