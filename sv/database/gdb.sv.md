{
  "date" : "2022-05-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GDB-filformat - ESRI-fil geodatabasfil",
  "description":"Läs mer om GDB-filformat och API:er som kan skapa och öppna GDB-filer.",
  "linktitle" : "GDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2022-05-08"
}

## Vad är en GDB fil?

ESRI-fil Geodatabase (FileGDB) är en samling filer i en mapp på skiva som innehåller relaterade geospatiala data såsom funktionsdatauppsättningar, funktionsklasser och tillhörande tabeller. Det kräver att vissa andra filer förvaras bredvid .gdb-filen i samma katalog för att det ska fungera. Frågor kan köras på .gdb-filen för att hantera rumslig såväl som icke-rumslig data.

## GDB-filformat - Mer information

Filgeodatabaser består av sju systemtabeller plus användardata. Användardata kan lagras i följande typer av datauppsättningar:

* Funktionsklass
* Funktionsdatauppsättning
* Mosaikdatauppsättning
* Rasterkatalog
* Rasterdatauppsättning
* Schematisk datauppsättning
* Tabell (icke-rumslig)
* Verktygslådor

Funktionsdatauppsättningar kan innehålla funktionsklasser såväl som följande typer av datauppsättningar:

* Bilagor
* Funktionslänkad kommentar
* Geometriska nätverk
* Nätverksdatauppsättningar
* Pakettyger
* Relationsklasser
* Terräng
* Topologier

Den maximala standardstorleken på datamängder i filgeodatabaser är 1 TB. Den maximala storleken kan ökas till 256 TB för stora datamängder (vanligtvis raster). Detta styrs av ett konfigurationsnyckelord. Se Konfigurationsnyckelord för filgeodatabaser för mer information.

Filgeodatabaser kan också innehålla undertyper och domäner och delta i utchecknings-/incheckningsreplikering och enkelriktade repliker.

En fil geodatabas kan nås samtidigt av flera användare. Om användarna redigerar måste de redigera olika datamängder.

## GDB-filformatspecifikationer ##

Fil GDB är ESRI-format och dess specifikationer är inte tillgängliga för allmänheten. På grund av denna anledning kunde inte filformatsinformationen för FIle GDB dokumenteras någon annanstans än vissa källor som har gjort det [delvis](https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec) genom omvänd konstruktion .

## Referenser ##

* [FGDB-specifikationer](https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec)

