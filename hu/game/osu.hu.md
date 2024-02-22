{
  "date" : "2023-01-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Ismerje meg az OSU fájlformátumot és az API-kat, amelyek OSU fájlokat hozhatnak létre és nyithatnak meg.",
  "title" : "OSU Fájl - Osu! Script fájl formátum",
  "linktitle" : "OSU",
  "menu" : {
    "docs" : {
      "identifier":"game-osu-hu",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-18"
}

## Mi az OSU fájl?

Az OSU fájl egy Osu számára írt játékszkript! ritmus játék. Információkat tartalmaz a játékban használt beatmap-ről, például a nehézségi szintről, a lejátszandó dalról és az eltalált tárgyak időzítéséről, amelyekhez a játékosnak szinkronizálnia kell a zenével. Lehetővé teszi a ritmusjátékosok számára, hogy egyéni kihívásokat dolgozzanak ki, és megosszák a játékközösséggel.

**OSR fájlformátum MIME típusa:** x-osu-beatmap

## OSU fájlformátum

Az OSU fájlok egyszerű szöveges fájlokként kerülnek elmentésre a lemezre, és szerkezetüket nagyon egyértelműen meghatározza a [OSU file format](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29) by osu!.

### Az OSU fájl szakaszai

Egy tipikus OSU fájl a következő részekkel rendelkezik.

|Szakasz |Leírás |Tartalom típusa|
---|---|---|
|[Általános]| Általános információk a beatmap-ről| kulcs: értékpárok|
|[Szerkesztő]| A beatmap szerkesztő mentett beállításai| kulcs: értékpárok|
|[Metaadatok] |A beatmap azonosítására használt információ| kulcs:érték párok|
|[Nehézség] |Nehézségi beállítások| kulcs:érték párok|
|[Események]| Beatmap és storyboard grafikai események| Vesszővel elválasztott listák|
|[Időpontok]| Időzítés és ellenőrzési pontok| Vesszővel elválasztott listák|
|[Színek]| Kombinált és bőrszínek| kulcs : értékpárok|
|[HitObjects]| Találat tárgyak| Vesszővel elválasztott listák|

## Hivatkozások

* [OSU! Ritmusjáték](https://osu.ppy.sh/home)

* [OSU fájlformátum](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29)


