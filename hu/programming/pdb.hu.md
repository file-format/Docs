{
  "date" : "2019-10-11",
  "keywords": [ "pdb file", "pdb", "extension", "format", "What is a pdb file", "pdb file format", "PDB metadata" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PDB fájlformátum – programadatbázis-fájl",
  "description":"További információ a PDB fájlformátumról és az API-król, amelyek PDB fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "PDB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Mi az a PDB fájl?

A .pdb kiterjesztésű fájl egy programadatbázis-fájl, amely egy lefordított futtatható fájl (EXE/DLL) hibakeresési információit tartalmazza. A PDB fájlokat a Microsoft Compilers állítja elő, amikor egy alkalmazást hibakeresési módban fordítanak. A PDB fájl jelenléte segíthet a végrehajtható fájl visszafejtésében, mivel jelentős információkat tartalmaz a modulok összes szimbólumáról. Ez az oka annak, hogy ezeket a fájlokat külön kell tartani a végső végrehajtható fájltól. A Microsoft [DgbHelp API](https://learn.microsoft.com/en-us/windows/win32/debug/dbghelp-functions) megnyithat egy PDB-fájlt, hogy olyan információkat szerezzen be, mint például a nyilvános és exportált adatok, globális szimbólumok, helyi szimbólumok, írja be az adatokat, a forrásfájlokat és a sorszámokat.

## PDB fájl formátum

A PDB a Microsoft szabadalmaztatott fájlformátuma, és hivatalosan még nem dokumentálták sehol. A kezdő dokumentáció azonban [itt](https://github.com/Microsoft/microsoft-pdb) érhető el, és hivatkozhat rá.

### EKT-folyamok

Az PDB-fájlok több adatfolyamból állnak, ahol mindegyik adatfolyam virtuális egyedi fájlként működik, és információkat tartalmaz. A PDB fájlírók írhatnak ezekre a fájlokra, és a fájl véglegesítése csak az explicit véglegesítés után történik meg. A fordító továbbra is írhat egy PDB fájlba, de csak akkor hajtja végre a véglegesítést, ha az összes felhasználói kód fordítása sikeres volt. Egy PDB fájl a következő adatfolyamokból áll:

|Stream száma |Tartalom |Rövid leírás|
---|---|---|
|1| Pdb (fejléc) |Verzióinformációk és információk az EKT-nek az EXE-hez való csatlakoztatásához|
|2| Tpi (Típuskezelő) |A végrehajtható fájlban használt összes típus.|
|3| Dbi (Hibakeresési információ) |A szekcióhoz való hozzájárulást és a 'Modok' listáját tartalmazza|
|4| Névtérkép| Kivonatos string táblázatot tart|
|4-(n+4)| n Mod's (Modulinformáció)| Minden Mod adatfolyam egy összeállításhoz tartalmaz szimbólumokat és sorszámokat
|n+4| Globális szimbólum hash| Egy index, amely lehetővé teszi a globális szimbólumokban való keresést név szerint|
|n+5| Nyilvános szimbólum hash| Egy index, amely lehetővé teszi a nyilvános szimbólumokban címek szerinti keresést|
|n+6| Szimbólum rekordok| A globális és nyilvános szimbólumok tényleges szimbólumrekordjai|
|n+7| Írja be a hash| A TPI adatfolyam által használt hash.|

Egy PDB-fájl minden adatfolyama több oldalból áll, amelyek nem feltétlenül vannak számozva egymás után.

### EKT fejléc

A PDB-fájl fejléccel rendelkezik, amely egy aláírásból áll az adott formátum azonosítására és érvényesítésére. Az aláírás hossza a PDB formátumától függ. A fejléc hosszabb lehet, mint egy oldal.

### EKT metaadatok
A PDB metaadatok felelősek az összes összetevő adatfolyam felismeréséért, megadva az egyes adatfolyamokhoz tartozó oldalak hosszát és sorrendjét. A parancsokat a folyamok egymás után kapják; 0-val kezdődik. Van egy rendezetlen gyökérfolyam is, amely a metaadatok egy részét tartalmazza.

## Hivatkozások
* [PDB – Wikipédia](https://en.wikipedia.org/wiki/Program_database)
* [Microsoft PDB](https://github.com/Microsoft/microsoft-pdb)

