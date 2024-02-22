{
  "date": "2022-12-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Ismerje meg az MCR fájlformátumot és az API-kat, amelyek MCR-fájlokat hozhatnak létre és nyithatnak meg.",
  "title": "MCR - Minecraft régió fájlformátuma",
  "linktitle": "MCR",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-mc-hur"
}
},
  "lastmod": "2022-12-14"
}

## Mi az MCR fájl?

A Minecraft MCR fájlformátum egy adatformátum, amelyet a Minecraft használ a Minecraft világ terepdarabjainak tárolására. Az NBT (Named Binary Tag) formátumon alapul, amelyet a népszerű nyílt forráskódú játékmotor, a Minecraft Forge fejlesztői fejlesztettek ki. Az MCR fájltípust a legelején vezették be, és később a [MCA file format](/game/mca/) váltotta fel.

## MCR fájlformátum

Az MCR fájlformátum elnevezett bináris címkék sorozataként épül fel, amelyek mindegyike meghatározott típusú adatokat tartalmaz. A legfelső szintű címke a Level címke, amely egyetlen játékszint összes adatát tartalmazza. A Level címkén belül számos más nevű címke található, amelyek különböző típusú adatokat tárolnak, mint például a Data címke, amely a játék világáról tárol információkat, valamint az Entities és TileEntities címkék, amelyek a játék világáról tárolnak adatokat. játéktárgyak és csempe entitások a világon, ill.

## Mi van az MCR fájlformátumban?

A Minecraft MCR fájlformátumban a régió a játékvilág 32x32-es blokkterülete. Az MCR formátum régiókra osztja a játékvilágot az adatok hatékonyabb kezelése és a játékszintek gyorsabb betöltése és mentése érdekében. Minden régió külön fájlban van tárolva, és az MCR fájlformátum egy koordinátarendszert használ az egyes régiók helyzetének azonosítására a játékvilágon belül. Egy régió koordinátáit a tartomány bal alsó sarkának blokkkoordinátái határozzák meg. Például egy (-1,0) koordinátákkal rendelkező régió egy régióval balra, nulla régióval lejjebb található a játék világának eredetétől.

## Az MCR fájlformátum specifikációi

Az MCR fájlformátum specifikációi nyilvánosan elérhetők. Az NBT formátum specifikációi, amelyeken az MCR formátum alapul, elérhetők a Minecraft Forge webhelyén. Ezenkívül a [Minecraft Wiki](https://minecraft.fandom.com/wiki/Region_file_format) részletes információkat tartalmaz az MCR fájlformátumról, beleértve annak szerkezetét és a támogatott különféle adattípusokat.

### Tömörített adatok az MCR-fájlokban

A Minecraft MCR fájlformátum támogatja a tömörítést. Az MCR fájlformátum a The [NBT format](https://minecraft.fandom.com/wiki/NBT_format)-on alapul, amely lehetővé teszi az adatok tömörített formában történő tárolását. Ez segít csökkenteni az MCR-fájlok méretét, és hatékonyabbá teszi az átvitelt és tárolásukat. Ez az MCR fájlformátum egyik fontos jellemzője, mivel lehetővé teszi a játékosok számára, hogy nagyméretű Minecraft World terepadatokat osszanak meg másokkal.

## Hivatkozások

* [A Minecraft világszerkesztője](https://www.mcedit.net/)

* [A Minecraftról](https://www.minecraft.net/)

* [Region File Format](https://minecraft.fandom.com/wiki/Region_file_format)

* [NBT formátum](https://minecraft.fandom.com/wiki/NBT_format)


