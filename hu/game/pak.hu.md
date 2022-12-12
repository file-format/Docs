{
  "date" : "2021-10-20",
  "keywords" :[ ".pak", "file format", "mi az a pak fájl", "fájl", "pak példa", "Video Game Package File", "extension"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ a .pak fájlokról és az API-król, amelyek PAK-fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"PAK fájlformátum - videojáték-csomagfájl",
  "linktitle" : "PAK",
  "menu" : {
    "docs" : {
      "identifier":"game-pak",
      "parent" : "game"
}
},
  "lastmod" : "2021-10-27"
}

## Mi az a PAK fájl?

A PAK-fájl egy csomagfájl, amelyet különböző videojátékok hoztak létre a játékadatok archiválására. Lényegében ez egy játék fájlformátum. Ez tartalmazhat több játékelemet, például grafikát, textúrákat, hangokat, tárgyakat, valamint egyéb játékadatokat. Az archívumot többnyire .zip fájlként mentik, és kibonthatók olyan népszerű kicsomagoló szoftverekkel, mint a WinZip és a WinRAR. PAK-fájlokat használó videojátékok például a Quake, a Hexen, a Crysis és a Half-Life.

## PAK fájlformátum - További információ

A legtöbb esetben a PAK-fájlokat [ZIP-fájlformátum](/hu/compression/zip/) formátumban menti a rendszer. A különböző alkalmazások azonban eltérő fájlformátumot használhatnak a fájlok tárolására.


## Hogyan lehet megnyitni a PAK fájlokat?

A PAK-fájlokat olyan alkalmazásokkal nyithatja meg, mint a [PakExplorer](https://www.quaketerminus.com/tools.shtml) és a [SpriteExplorer](http://www.slackiller.com/hlprograms.htm).

**------------------------------------------------- -------------------------------------------------- -----------------------**

## PAK fájlformátum - Simutrans objektumfájl

A .pak kiterjesztésű fájl egy [Simutrans](https://www.simutrans.com/en/) közlekedési szimulációs játék fájlformátuma. A szimulációban használt objektumokat, például felhasználó által készített grafikákat és adattartalmakat tartalmaz. Számos különböző objektumot tartalmazhat, például játékjárműveket, épületeket, terepeket stb. A PAK-fájlokat a MakeObject segédprogrammal állítják elő, amely .dat fájlokat és .png képeket állít össze a szimulációs objektumok létrehozásához. A Simutrans lehetővé teszi a játékosok számára, hogy sikeres közlekedési rendszert vezessenek be az utasok, postai küldemények és áruk szárazföldi szállítási rendszereinek kiépítésével és kezelésével.

## Hogyan készítsünk PAK fájlokat?

A Simutrans mintapéldákat sorolt fel PAK-fájlok létrehozására Windows és Linux operációs rendszeren.

### Windows operációs rendszer

```
simutrans_src
   makeobj.exe
   haus_01
        haus_01.dat
        haus_01.png
        pak.bat
   auto_03
        auto_03.dat
        auto_03.png
        pak.bat
   triebzug_01
        triebzug_vorn.dat
        triebzug_mitte.dat
        triebzug_hinten.dat
        triebzug_01.png
        pak.bat
```
### Linux BE/OS

```
simutrans_src
   makeobj
   haus_01
        haus_01.dat
        haus_01.png
        pak
   auto_03
        auto_03.dat
        auto_03.png
        pak
   triebzug_01
        triebzug_v.dat
        triebzug_m.dat
        triebzug_h.dat
        triebzug_01.png
        pak
```

## Hivatkozások

* https://simutrans-germany.com/wiki/wiki/en_doPak
* https://en.wikipedia.org/wiki/Simutrans

