{
  "date" : "2019-12-10",
  "keywords" :[ "XLTM", "file", "extension", "file format", "Excel Open XML Macro", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"A fájlformátum útmutatója, hogy megtudja, mi az XLTM fájl és API-k, amelyek létrehozhatják és megnyithatják azokat.",
  "title" :"What is an XLTM file?",
  "linktitle" : "XLTM",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Mi az XLTM fájl?

Az XLTM fájlkiterjesztés azokat a fájlokat jelöli, amelyeket a Microsoft Excel hoz létre makró-kompatibilis sablonfájlként. Az XLTM-fájlok hasonlóak az [XLTX]-hez (/hu/spreadsheet/xltx/) más szerkezetben, mint hogy a későbbiek nem támogatják a makrókat tartalmazó sablonfájlok létrehozását. Az ilyen sablonfájlokat az elrendezés, a formázás és egyéb beállítások generálására és beállítására használják a makrók mellett, hogy megkönnyítsék a hasonló XLSX-fájlok létrehozását.

## Rövid története ##

2000 elején a Microsoft a változtatás mellett döntött, hogy megfeleljen az **Office Open XML** szabványnak. Az új szabvány szerinti különböző típusú dokumentumokat úgy azonosították, hogy "X"-et fűztek a kiterjesztéseikhez, ahol az "X" az XML-t jelenti. 2007-re ez az új fájlformátum az Office 2007 részévé vált, és a Microsoft Office új verzióiban is érvényesül. Az új fájltípus további előnyökkel jár a kis fájlméret, a kisebb sérülések és a jól formázott képek megjelenítése miatt.

## XLTM fájlformátum specifikációi ##

Az XLTM fájlok az Office OpenXML fájlformátumon alapulnak, és XML-t és [ZIP]-et (/hu/compression/zip/) használnak a fájlméret csökkentésére. Ezeket a fájlra dupla kattintással Microsoft Excel programmal lehet megnyitni. A fájlok XLTM fájlformátumban történő szervezését úgy figyelheti meg, hogy a fájlt átnevezi ZIP-re, majd kicsomagolja a tartalmát a lemezre.

### [Content_Types].xml ###

Ez az egyetlen fájl, amely az alapszinten található a zip kicsomagolásakor. Felsorolja a csomagon belüli részek tartalomtípusait. Ebben az XML-fájlban minden, a csomagban található XML-fájlra való hivatkozás hivatkozik.

### \_rels (mappa) ###

Ez a Relationships mappa, amely egyetlen XML-fájlt tartalmaz, amely a csomagszintű kapcsolatokat tárolja. Az Xltx fájlok kulcsfontosságú részeire mutató hivatkozásokat ez a fájl URI-ként tartalmazza. Ezek az URI-k azonosítják az egyes kulcselemek kapcsolatának típusát a csomaggal. Ez magában foglalja az xl/workbook.xml formátumban található elsődleges irodai dokumentumhoz és a docProps egyéb részeihez való viszonyt, mint alapvető és kiterjesztett tulajdonságokat.

### docProps ###

Ez a mappa tartalmazza a dokumentum általános tulajdonságait. Ezek közé tartozik az alapvető tulajdonságok készlete, a kiterjesztett vagy alkalmazásspecifikus tulajdonságok készlete, valamint a dokumentum miniatűr előnézete. Egy üres munkafüzet két fájlt tartalmaz ebben a mappában: app.xml és core.xml. A core.xml olyan információkat tartalmaz, mint a szerző, a létrehozás és mentés dátuma, valamint a módosítás. Az App.xml információkat tartalmaz a fájl tartalmáról.

### xl (mappa) ###

Ez a fő mappa, amely a munkafüzet tartalmával kapcsolatos összes részletet tartalmazza. Alapértelmezés szerint a következő mappákkal rendelkezik:

* \_rels
* téma
* munkalapok

és a következő xml fájlok:

* styles.xml
* munkafüzet.xml

## Hivatkozások ##

* [MS-XLSX fájlformátum](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

