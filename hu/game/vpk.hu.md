{
  "date" : "2023-01-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Ismerje meg az Unreal Static Meshes VPK fájlformátumot és az API-kat, amelyek VPK-fájlokat hozhatnak létre és nyithatnak meg.",
  "title" : "VPK fájl – irreális statikus hálófájl",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "identifier":"game-vpk-hu",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-16"
}

## Mi az a VPK fájl?

A .vpk fájl a **Source Engine**, a Valve Corporation által kifejlesztett játékmotor által használt fájlformátum. A VPK-fájlokat játéktartalom, például modellek, textúrák és hangok csomagolására használják, és gyakran használják olyan játékokban, mint a Team Fortress 2, a Left 4 Dead és a Counter-Strike: Global Offensive. A fájlok számos eszközzel megnyithatók és kibonthatók, például a GCFScape és a VPK Tool segítségével.

## VPK fájlformátum - További információ

A VPK fájlok bináris fájlokként kerülnek a lemezre. Egyetlen vpk-fájl lehet egy VPK-csomag része, vagy működhet független nyers VPK-fájlként. A VPK-fájlban tárolható információk között szerepelnek térképek, anyagok, játéktartalom és koreográfiai jelenetek.

### Hogyan készítsünk VPK fájlt?

A rendelkezésre álló eszközöktől függően többféleképpen is létrehozhat .vpk fájlt.

1. `A VPK eszköz használata:` Ez egy parancssori eszköz, amely VPK fájlok létrehozására és kibontására használható. A VPK fájl a következő paranccsal hozható létre:
```
"vpk.exe -M <directory> <output_file.vpk>"
```
Ezzel létrehoz egy VPK-fájlt a megadott könyvtárból, és elmenti a megadott kimeneti fájlként.

1. `A Hammer Editor használata:` A Hammer Editor egy olyan eszköz, amely a Source SDK részét képezi, és amellyel a Source motort használó játékok szintjeit lehet létrehozni és szerkeszteni. Lehetővé teszi VPK fájlok létrehozását is, ha jobb gombbal kattint egy mappára a Fájlrendszer lapon, és válassza a VPK létrehozása lehetőséget.

1. A Valve VPK készítőjének használata: Ez a Valve által kifejlesztett eszköz, amelyet játéktartalom csomagolására és terjesztésére használnak. Ez az eszköz használható VPK fájlok létrehozására, és egyben a VPK fájlok létrehozásának hivatalos eszköze is.

## Hivatkozások

 * [Valve Software](https://www.valvesoftware.com/en/)
 * [VPK fejlesztői források](https://developer.valvesoftware.com/wiki/GCF)

