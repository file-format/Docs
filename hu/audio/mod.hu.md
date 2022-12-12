{
  "date" : "2021-08-04",
  "keywords" :[ "mod", "mp3", "fájl", "kiterjesztés", "formátum", "mi a mod fájlformátum", "zene", "mod fájlformátum", "mod vs MP3", "mod fájlformátum specifikációja"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ a MOD fájlformátumról és az API-król, amelyek MOD fájlokat hozhatnak létre, konvertálhatnak és megnyithatnak.",
  "title" :"MOD - zenei modul fájl",
  "linktitle" : "MOD",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-04"
}

## Mi az a MOD fájl?
A .mod kiterjesztésű fájl a szabványos zenei modul formátum használatával létrehozott zenei modul fájl, amely a Karsten Obarski által kifejlesztett **Amiga modul formátumon** alapul, és az **Ultimate Soundtracker** szoftverrel került kiadásra a Commodore számára. Amiga rendszer. A [MIDI](/hu/audio/mid/) fájlhoz hasonlóan hangmintákat és hangmintákat tartalmaz, amelyek különböző hangszereket képviselnek, amelyeket a hangok szerint játszanak le. A MOD fájlokat különösen a videojátékokban használják háttérzeneként és a **demoscene** számítógépes művészeti szubkultúrában.

## MOD fájl formátum

A MOD egy számítógépes fájlformátum, amelynek alapvető funkciója a zene megjelenítése, és ez volt az első modul fájlformátum. A MOD-fájlok a .mod fájlkiterjesztést használják, kivéve az **Amiga**-t, amely beolvassa a fájl fejlécét a fájltípus meghatározásához, így nem támaszkodik a fájlnév-kiterjesztésekre. A MOD fájl különböző hangszerek készletéből áll minták formájában, számos mintából, amelyek meghatározzák, hogyan és mikor kell lejátszani a mintákat, valamint egy listát arról, hogy milyen mintákat milyen sorrendben kell lejátszani.

### A MOD fájlformátum specifikációi

A MOD fájl mintázat valójában egy szekvenszer felhasználói felületen egy táblázatként van kialakítva, csatornánként egy oszloppal, tehát ez a táblázat négy oszlopból áll (egy minden Amiga hardvercsatornához. Minden oszlop 64 sorból áll).

A táblázat egy cellája a következő műveletek egyikét okozhatja oszlopának csatornáján, amikor eléri a sor idejét:

- Indítson el egy hangszert, amely új hangot játszik ezen a csatornán adott hangerőn, esetleg speciális effektussal
- Módosítsa az aktuális hangjegyre alkalmazott hangerőt vagy speciális effektust
- Változás minta áramlás; ugorjon egy adott dal vagy minta pozícióra, vagy hurok egy mintán belül
- Ne csinálj semmit; az ezen a csatornán lejátszott hangjegyek lejátszása folytatódik

A műszer egyetlen minta, opcionálisan megadva, hogy a minta mely része ismételhető meg, hogy szilárd hangot tartson fenn.

### Időzítés
A minimális időkeret 0,02 másodperc volt az eredeti MOD fájlban, vagy egy "függőleges kiürítési" (VSync) intervallum, mivel az eredeti szoftver a monitor VSync időzítését használta 50 Hz-en (PAL) vagy 60 Hz-en (NTSC esetén). az időzítéshez.

## Hivatkozások

* [MOD (fájlformátum) – a Wikipédia által](https://en.wikipedia.org/wiki/MOD_(file_format))

