{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Ismerje meg az OSR fájlformátumot és az API-kat, amelyek OSR-fájlokat hozhatnak létre és nyithatnak meg.",
  "title" : "OSR fájl - osu! Fájlformátum újrajátszása",
  "linktitle" : "OSR",
  "menu" : {
    "docs" : {
      "identifier":"game-osr-hu",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Mi az az OSR fájl?

An OSR file is a game replay file created by the [osu! game](https://osu.ppy.sh/home). Osu! is a rhythm game where users match mouse clicks with the music. The song played by the user, hits and misses, time and date of song played, and overall ranking is recorded in the OSR file. This OSR file can then be shared with others for replay purpose. OSR file requires the beatmap file to be present in the "Songs" folder.

** MIME típusú OSR fájlformátum:** x-osu-replay

## OSR fájlformátum

Az OSR-fájlok bináris fájlként kerülnek mentésre rögzített és változó hosszúságú adatmezőkkel.

|Adattípus| Formátum|
---|---|
|Bájt |Az újrajátszás játékmódja (0 = osu! Standard, 1 = Taiko, 2 = Catch the Beat, 3 = osu!mánia)|
|Integer |A játék azon verziója, amikor az újrajátszást létrehozták (pl. 20131216)|
|Húr |osu! beatmap MD5 hash|
|Húr| Játékos neve|
|Húr| osu! replay MD5 hash (beleértve a visszajátszás bizonyos tulajdonságait)|
|Rövid| 300-asok száma|
|Rövid| Szabványban 100, Taikoban 150, CTB-ben 100, mániában 100 mp|
|Rövid| 50-esek száma standardban, kis gyümölcsök CTB-ben, 50-es mániában|
|Rövid| Gekik száma szabványban, Max 300 mániában|
|Rövid| Katusok száma standardban, 200 mániában|
|Rövid| Kihagyások száma|
|Egész szám| Az eredményjelentésben megjelenített összpontszám|
|Rövid| A legjobb kombináció a pontszámjelentésben|
|Bájt| Tökéletes/teljes kombó (1 = nincsenek kihagyások, nincsenek csúszkatörések és nincsenek korán befejezett csúszkák)|
|Egész szám| Használt modok. Lásd alább a mod értékek listáját.|
|Húr| Élettartam oszlopdiagram: vesszővel elválasztott u/v párok, ahol u a dalba jutási idő ezredmásodpercben, v pedig egy 0 és 1 közötti lebegőpontos érték, amely az adott időpontban eltöltött életmennyiséget jelöli (0 = életsáv üres, 1= életsáv megtelt)|
|Hosszú| Időbélyegző (Windows ketyeg)|
|Egész szám| A tömörített visszajátszási adatok hossza bájtban|
|Bájt |Tömb Tömörített visszajátszási adatok|
|Hosszú| Online Score ID|
|Kettős| További mod információk. Csak akkor jelenik meg, ha a Target Practice engedélyezve van.|

## Hivatkozások

* [OSU! Ritmusjáték](https://osu.ppy.sh/home)

* [OSR-fájlformátum](https://osu.ppy.sh/wiki/en/Client/File_formats/Osr_%28file_format%29#data-types)


