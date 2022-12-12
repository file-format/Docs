{
  "date" : "2021-08-09",
  "keywords" :[ "mmf", "file", "extension", "format", "audio", "smaf", "mmf extension", "mmf files", "mobile music file", "yamaha"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ az MMF fájlformátumról és az MMF-fájlok létrehozására és megnyitására alkalmas API-król.",
  "title" :"MMF – mobil zenei fájlformátum",
  "linktitle" : "MMF",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-09"
}

## Mi az MMF fájl?

Az MMF egy SMAF fájlhoz társított fájlkiterjesztés. Az MMF a Mobile Music File, míg az SMAF a szintetikus zenei mobilalkalmazás formátum rövidítése. Az okostelefonon belüli MMF-fájlok rendszercsengőhangokat, hangot, valamint grafikát és szöveges megjelenítést tartalmazhatnak. Az MMF továbbá háromféle műszerparamétert tartalmaz, beleértve az FM-et, a PCM-et és a Stream PCM-et. Ezek a fájlformátumok kompatibilisek a Windows rendszerplatformmal. Az MMF-fájlok adatfájlokként vannak besorolva. A Microsoft Mail általában támogatja az MMF-fájlokat. Az MMF utótaggal rendelkező fájl bármely mobileszközre vagy rendszerplatformra másolható.

Ráadásul ezek a fájlok sokkal kisebb méretűek a szabványos MIDI formátumú fájlokhoz képest. A [WAV](/hu/audio/wav/) és [MID](/hu/audio/mid/) fájlok MMF formátumba konvertálhatók, majd megoszthatók és audiotartalomként terjeszthetők. Ezeket a fájlokat e-mailben közvetlenül telefonra és számítógépre is megkaphatja.


## Az MMF fájlformátum rövid története

A Yamaha az SMAF-eszközöket hangfájlként fejlesztette ki, hogy az okostelefonok több egyedi csengőhangot tárolhassanak. A Yamaha az MA-1, MA-2, MA-3, MA-5 és MA-7 LSI hangchipek gyártásával mutatta be az SMAF-ot. Mindezek a formátumok meglehetősen ismertté váltak a kelet-ázsiai piacon a mobiltelefonok körében 2000 elején.

Nemzetközi szinten az MMF formátumot a Samsung engedélyezte. Az MMF formátum segítségével a Samsung a többszólamú csengőhangok széles skáláját tudta megtervezni a Samsung okostelefonokban való használatra.

A Yamaha a formátumot még népszerűbbé akarta tenni, így a hivatalos Yamaha SMAF fájlokon több, ezzel a formátummal kompatibilis eszközt tett közzé. Ezzel a felhasználók könnyedén lejátszhatják az MMF fájlokat a számítógépükön.


## MMF fájlformátum specifikációi ##

Az MMF-fájlok adatrészekbe vannak sorolva. Az egyes szegmensek leírására egy 8 bájt körüli prefix szerkezetet használnak.
A 4 bájtos címke tartalmazza a CNTI-t, az OPDA-t, az MSTR-t, az MTR-t és az ATR-t. Az adatméret plusz 8 bájt a csonk mérete; a teljes fájlméretet az összes darabméret összegzésével számítjuk ki. Ha egy fájl nem sérült, az összegzett fájlméretnek meg kell egyeznie az elsődleges fejléc méretével.

### Fejléc ###

```
struct SMAF_Header
{
    uint32   SignatureMMMD;     // Signature: "MMMD"
    uint32   SizeSMAF;      // 4 byte data size, big-endian order
};
```

Íme egy példa az MMF fájlra:

![](../mmf.png)

## Hivatkozások

* [MMF – a Wikipedia által](https://en.wikipedia.org/wiki/Synthetic_music_mobile_application_format)

