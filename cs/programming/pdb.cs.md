{
  "date" : "2019-10-11",
  "keywords": [ "pdb file", "pdb", "extension", "format", "What is a pdb file", "pdb file format", "PDB metadata" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru PDB - soubor databáze programu",
  "description":"Další informace o formátu souboru PDB a rozhraních API, která mohou vytvářet a otevírat soubory PDB.",
  "linktitle" : "PDB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Co je soubor PDB?

Soubor s příponou .pdb je soubor databáze programu, který obsahuje informace o ladění kompilovaného spustitelného souboru (EXE/DLL). Soubory PDB jsou generovány kompilátory společnosti Microsoft, když je aplikační program kompilován v režimu ladění. Přítomnost souboru PDB může pomoci při zpětném inženýrství spustitelného souboru, protože obsahuje významné informace o všech symbolech modulů. Z tohoto důvodu jsou tyto soubory uchovávány odděleně od konečného spustitelného souboru. Microsoft [DgbHelp API](https://learn.microsoft.com/en-us/windows/win32/debug/dbghelp-functions) může otevřít soubor PDB a získat informace, jako jsou publics a exports, globální symboly, místní symboly, typová data, zdrojové soubory a čísla řádků.

## Formát souboru PDB

PDB je proprietární formát souborů společnosti Microsoft a dosud nebyl nikde oficiálně zdokumentován. Úvodní dokumentace je však k dispozici [zde](https://github.com/Microsoft/microsoft-pdb) a lze na ni odkazovat.

### Streamy PDB

Soubory PDB se skládají z více proudů, kde každý proud funguje jako virtuální samostatný soubor a obsahuje informace. Zapisovatelé souborů PDB mohou zapisovat do těchto souborů a soubor je finalizován pouze po vydání explicitního potvrzení. Kompilátor může pokračovat v zápisu do souboru PDB, ale odevzdat jej pouze v případě, že se veškerý uživatelský kód zkompiluje úspěšně. Soubor PDB se skládá z následujících streamů:

|Číslo proudu |Obsah |Krátký popis|
---|---|---|
|1| Pdb (záhlaví) |Informace o verzi a informace pro připojení tohoto PDB k EXE|
|2| Tpi (Správce typů) |Všechny typy použité ve spustitelném souboru.|
|3| Dbi (Informace o ladění) |Uchovává příspěvky sekce a seznam 'Mods'|
|4| Mapa jmen| Obsahuje tabulku hashovaných řetězců|
|4-(n+4)| n Mod's (informace o modulu)| Každý Mod stream obsahuje symboly a čísla řádků pro jednu kompilaci|
|n+4| Globální symbol hash| Index, který umožňuje vyhledávání v globálních symbolech podle názvu|
|n+5| Hash veřejného symbolu| Index, který umožňuje vyhledávání ve veřejných symbolech podle adres|
|n+6| Záznamy symbolů| Aktuální záznamy symbolů globálních a veřejných symbolů|
|n+7| Zadejte hash| Hash používaný streamem TPI.|

Každý proud v souboru PDB se skládá z několika stránek, které nemusí být nutně postupně číslovány.

### Záhlaví PDB

Soubor PDB je s hlavičkou, která se skládá z podpisu pro identifikaci a ověření konkrétního formátu. Délka podpisu závisí na formátu PDB. Záhlaví může být delší než jedna stránka.

### Metadata PDB
Metadata PDB jsou zodpovědná za rozpoznání všech dílčích toků, přičemž u každého toku udává délku a sekvenci stránek. Příkazy se zadávají proudům postupně; počínaje 0. Existuje také neuspořádaný kořenový proud, který obsahuje některá metadata.

## Reference
* [PDB – Wikipedia](https://en.wikipedia.org/wiki/Program_database)
* [Microsoft PDB](https://github.com/Microsoft/microsoft-pdb)

