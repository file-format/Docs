{
"dátum": "2023-09-27",
  "keywords": [
"cfg",
"cfg fájl",
"cfg mame konfigurációs fájl",
"mi az a cfg fájl",
"hogyan kell megnyitni a cfg fájlt",
"fájl",
"cfg fájlkiterjesztés",
"kiterjesztés"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "CFG fájlformátum - MAME konfigurációs fájl",
  "description":"További információ a CFG MAME konfigurációs fájl formátumáról és az API-król, amelyek CFG fájlokat hozhatnak létre és nyithatnak meg.",
"linktitle": "CFG MAME",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-mame",
      "parent": "settings"
}
},
"lastmod": "2023-09-27"
}

## Mi az a CFG fájl?

A CFG fájl egy XML-billentyűzet konfigurációs fájl, amelyet a MAME arcade videojáték-emulátorok használnak. Kulcsfontosságú összetevő a billentyűzet vezérlőinek és gyorsbillentyűinek a játékos preferenciáinak megfelelő testreszabásához. Ezek a fájlok olyan leképezéseket és beállításokat tárolnak, amelyek meghatározzák, hogy a billentyűzet hogyan kommunikál az emulátorral játék közben. A fájl szerkesztésével a felhasználók személyre szabhatják játékélményüket azáltal, hogy speciális billentyűzetbillentyűket rendelnek hozzá a játékon belüli műveletekhez, például érmebeszúráshoz, indításhoz, mozgáshoz és számos egyéb funkcióhoz.

## MAME konfigurációs fájl

A MAME, amely a **Multiple Arcade Machine Emulator** rövidítése, egy olyan szoftveralkalmazás, amely lehetővé teszi, hogy arcade játékokat emuláljon és játszhasson a számítógépén. A MAME konfigurációs fájlokat használ viselkedésének és beállításainak testreszabásához. Ezek a konfigurációs fájlok általában a MAME könyvtár `cfg` mappájában találhatók.

Íme a fő konfigurációs fájlok, amelyekkel találkozhat a MAME beállításakor és konfigurálásakor:

1. **mame.ini:** Ez a MAME fő konfigurációs fájlja. Olyan globális beállításokat tartalmaz, amelyek minden játékra vonatkoznak. Ez a fájl a MAME telepítésének gyökérkönyvtárában található.

1. **default.cfg:** Ez a fájl az összes olyan játék alapértelmezett beállításait tárolja, amelyek nem rendelkeznek saját konfigurációs fájlokkal. A játékspecifikus beállítások tartalékaként használatos.

1. **game-specific.cfg:** Ezek a fájlok az egyes játékok beállításainak tárolására szolgálnak. Általában a hozzájuk tartozó játék ROM-fájlja után nevezik el őket. Például, ha a "pacman.zip" nevű játékod van, a konfigurációs fájl a "pacman.cfg" lesz.

Íme néhány általános beállítás, amelyet a MAME konfigurációs fájljában találhat.

1. **rompath:** Megadja azt a könyvtárat, ahol az arcade játék ROM-jai találhatók.

1. **cfg_directory:** Megadja azt a könyvtárat, ahol a játékspecifikus konfigurációs fájlok tárolódnak.

1. **nvram_directory:** Megadja azt a könyvtárat, ahol a nem felejtő RAM (NVRAM) fájlokat tárolja. Az NVRAM a rekordokat és más játékspecifikus adatokat tárolja.

1. **artwork_directory:** Megadja a grafikák (például keretek, sátrak és szórólapok) tárolási könyvtárát.

1. **samplepath:** Megadja azt a könyvtárat, ahol a mintahangfájlok találhatók.

1. **cheatpath:** Megadja azt a könyvtárat, ahol a csaló fájlok találhatók.

Különféle egyéb beállításokat is megadhat, például video- és hangbeállításokat, vezérlőket és beviteli eszközöket. A beállítások módosításához nyissa meg a konfigurációs fájlt a szövegszerkesztőben, és hajtsa végre a szükséges módosításokat.

## MAME

A MAME, amely a **"Multiple Arcade Machine Emulator"** rövidítése, egy szoftveralkalmazás, amelyet régi játéktermi gépek és játéktermi játékkonzolok hardverének emulálására és replikálására terveztek. Lehetővé teszi a felhasználók számára, hogy a klasszikus arcade játékok hatalmas könyvtárával játsszanak modern számítógépeken és más kompatibilis eszközökön. A MAME egy nyílt forráskódú projekt, és az arcade játékok gazdag történetének megőrzésére és élvezetére alkalmas emulátor lett.

1. **Emuláció:** A MAME elsődleges célja az arcade gépek hardverének pontos emulálása, beleértve a központi feldolgozó egységeiket (CPU-kat), a hangchipeket, a grafikus chipeket és a beviteli eszközöket. Ez a pontossági szint biztosítja, hogy a játékok a lehető legközelebb álljanak az eredeti játéktermi élményhez.

1. **Kompatibilitás:** A MAME arcade játék ROM-ok széles skáláját támogatja, így az egyik legátfogóbb arcade emulátor elérhető. Különféle játéktermi platformokról futtathat játékokat, beleértve a 70-es, 80-as, 90-es évek klasszikus játékait, és még néhány újabb játéktermi játékot is.

1. **Megőrzés:** A MAME egyik elsődleges küldetése az arcade játékok történetének megőrzése. A játéktermi hardverek pontos emulálásával a MAME segít megelőzni a klasszikus játékok elvesztését, és biztosítja, hogy a jövő nemzedékei úgy élhessék meg őket, ahogyan eredetileg tervezték.

1. **Front-Ends:** Sok felhasználó olyan front-end alkalmazásokat használ, amelyek grafikus felületet biztosítanak a játékok MAME-n keresztüli kezelésére és elindítására. Ezek a felületek megkönnyítik a navigálást a MAME kiterjedt játékkönyvtárában.

## CFG fájl - Mivel nyitható meg?

Olyan programok, amelyek megnyitják a CFG fájlokat vagy hivatkoznak rájuk

- MAME (ingyenes) (Windows)
- ExtraMAME (próba)
- MacMAME (MAC)

## Egyéb CFG fájlok

Íme más fájltípusok, amelyek a **.cfg** fájlkiterjesztést használják.

**Beállítások**
- [CFG - Celestia konfigurációs fájl](/hu/settings/cfg-celestia/)
- [CFG - Citrix Server Connection File](/hu/settings/cfg-citrix/)
- [CFG - MAME konfigurációs fájl](/hu/settings/cfg-mame/)
- [CFG - LightWave konfigurációs fájl](/hu/settings/cfg-lightwave/)

**Játszma, meccs**
- [CFG - Wesnoth Markup Language File](/hu/game/cfg-wesnoth/)
- [CFG - MUGEN konfigurációs fájl](/hu/game/cfg-mugen/)
- [CFG - Source Engine Configuration File](/hu/game/cfg-sourceengine/)

**Rendszer és egyéb**
- [CFG - CFG fájl](/hu/system/cfg/)
- [CFG - Cal3D modell konfigurációs fájl](/hu/misc/cfg-cal3d/)

## Hivatkozások
* [MAME](https://en.wikipedia.org/wiki/MAME)

