{
  "date" : "2021-04-15",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MPG fájlformátum",
  "keywords" :[ "MPG", "fájl", "kiterjesztés", "formátum", "videóformátum", "mi az mpg fájlformátum", "mpg fájlformátum", "mpg fájllejátszó", "mpeg tömörítés", "videó", "MPEG", "MPEG-1", "MPEG-2"],
  "description":"További információ az MPG fájlformátumról és az API-król, amelyek létrehozhatják és megmutathatják, hogyan kell megnyitni az MPG fájlokat.",
  "linktitle" : "MPG",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-07-26"
}

## Mi az MPG fájlformátum? ##

Az .mpg kiterjesztésű fájl az MPEG-1 vagy MPEG-2 audio- és videotömörítéshez tartozó fájlkiterjesztések csoportjába tartozik. Az MPEG-1 2. rész videója nem könnyen elérhető, és ez a kiterjesztés (MPG fájlformátum) általában az MPEG-1-ben és MPEG-2-ben meghatározott MPEG programfolyamra, vagy az MPEG-2-ben meghatározott MPEG szállítási adatfolyamra mutat. . Más kiterjesztések, például az .m2ts is léteznek, amelyek megadják a pontos tárolót, ebben az esetben az MPEG-2 TS, de ez kevéssé vonatkozik az MPEG-1 adathordozóra. Az [.mp3](https://docs.fileformat.com/audio/mp3/) az MP3 hangot tartalmazó fájlok leggyakoribb kiterjesztése. Az MP3 fájl a nyers hang tipikus adatfolyama; Az MP3 fájlok címkézésének hagyományos módja az, hogy a streamadatokat minden képkocka "szemét" szegmensébe írják, amelyek elmentik a médiainformációkat, de az **mpg fájllejátszó** eldobja azokat. Ez egy hasonló technika, amelyet az AAC-fájlok címkézésére használnak, de manapság kevésbé támogatott.

## MPEG tömörítés ##

Az MPEG név a Moving Pictures Experts Group rövidítése. Az MPEG egy videotömörítési eszköz, amely magában foglalja a képek és hangok tömörítését, valamint a kettő szinkronizálását.
Jelenleg számos MPEG szabvány létezik.

- Az MPEG-1 közepes adatátviteli sebességekhez javasolt, 1,5 Mbit/sec nagyságrendben.
- Az MPEG-2 nagy, legalább 10 Mbit/sec adatátviteli sebességhez javasolt.
- Az MPEG-3-at HDTV-tömörítésre javasolták, de redundánsnak találták, és egyesítették az MPEG-2-vel.
- Az MPEG-4 nagyon alacsony, 64 Kbit/s-nál kisebb adatsebességhez javasolt.


## MPG fájlformátumú programfolyam ##

A programfolyam egy tároló a digitális hang, videó és egyebek multiplexeléséhez. A Program Stream formátumát az MPEG-1 (ISO/IEC 11172-1) és az MPEG-2, Systems (ISO/IEC 13818-1/ITU-T H.222.0 szabvány) 1. része határozza meg. Az MPEG-2 Program Stream analóg alapú, hasonló az ISO/IEC 11172 Systems réteghez, és előre kompatibilis.

### Kódolási részletek ###

Íme a részleges MPEG-2 Program Stream csomag fejlécformátumának kódolási részletei:

| Név | Bitek száma | Leírás |
---|---|---|
| bájtok szinkronizálása | 32 | 0x000001BA |
| jelölő bitek | 2 | 01b az MPEG-2 verzióhoz. Az MPEG-1 verzió jelölőbitjei 4 bitek 0010b értékkel. |
| Rendszeróra [32..30] | 3 | System Clock Reference (SCR) bitek 32-30 |
| jelölő bit | 1 | 1 bit mindig beállítva. |
| Rendszeróra [29..15] | 15 | Rendszeróra bitek 29-15 |
| jelölő bit | 1 | 1 bit mindig beállítva. |
| Rendszeróra [14..0] | 15 | Rendszeróra bitek 14-től 0-ig |
| jelölő bit | 1 | 1 bit mindig beállítva. |
| SCR kiterjesztése | 9 | |
| jelölő bit | 1 | 1 bit mindig beállítva. |
| bitsebesség | 22 | 50 bájt/másodperc egységekben. |
| jelölő bitek | 2 | 11 bit mindig beállítva. |
| fenntartva | 5 | jövőbeli használatra fenntartva |
| töltelék hossza | 3 | |
| töltelék bájtok | 8*töltelék hossza | |
| rendszerfejléc (opcionális) | 0 vagy több | ha a rendszerfejléc kezdőkódja következik: 0x000001BB |

Az alábbi táblázat a részleges rendszerfejléc-formátumot mutatja:

| Név | Bájtok száma | Leírás |
---|---|---|
| bájtok szinkronizálása | 4 | 0x000001BB |
| fejléc hossza | 2 | |
| sebességkorlátozott és jelölőbitek | 3 | |
| hangkötés és zászlók | 1 | |
| zászlók, jelölő bit és videó bekötés | 1 | |
| Csomagsebesség korlátozás és lefoglalt bájt | 1 | |


## Referenciák ##

- [MPEG-1 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-1)



