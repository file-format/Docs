{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Ismerje meg az OSZ fájlformátumot és az API-kat, amelyek OSZ-fájlokat hozhatnak létre és nyithatnak meg.",
  "title" : "OSZ File - osu! Beatmap fájlformátum",
  "linktitle" : "OSZ",
  "menu" : {
    "docs" : {
      "identifier":"game-osz-hu",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Mi az OSZ fájl?

Az OSZ fájl az osu ritmusjáték által használt tömörített fájlformátum! beatmap adatok tárolására. Az ütemtérképek alapvetően a játék szintjei, és olyan információkat tartalmaznak, mint a dal, az ütemidő és a találati tárgyak elhelyezése a játék képernyőjén. Az OSZ fájlok lehetővé teszik a beatmapek egyszerű terjesztését, és általában az internetről töltik le és importálják a játékba. OSU! rendelkezik a [OSR](/game/osr/) fájlformátummal is, amely egy játékvisszajátszási fájl, és a játékosok újrajátszhatják.

**OSR fájlformátum MIME típusa:** x-osu-replay

## OSZ Fájlformátum

Az OSZ fájltípusok belső fájlformátum-adatai nem nyilvánosak. [ZIP](/compression/zip/)-tömörített adatokat tartalmaz, amelyek információkat tartalmaznak a zene lejátszásához, a grafikák megjelenítéséhez és a lejátszók megjelenítéséhez azokról az eseményekről, amikor interakcióba kell lépniük a játékkal.

## Hogyan készítsünk OSZ fájlt?

OSU! részletes utasításokat tartalmaz a [creating OSZ](https://osu.ppy.sh/wiki/en/Client/File_formats#creating-.osz-and-.osk-files) és az OSK fájlokhoz. A következő lépésekkel hozhat létre OSZ fájlt az OSU! segítségével.

1. Nyisson meg egy ütemtérképet a szerkesztőn keresztül.
1. A felső menüből válassza a Fájl > Csomag exportálása... menüpontot.
1. Az .osz archívum a osu! mappát.

## Hivatkozások

* [OSU! Ritmusjáték](https://osu.ppy.sh/home)


