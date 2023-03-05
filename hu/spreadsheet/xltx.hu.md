{
  "date" : "2019-12-10",
  "keywords" :[ "XLTX", "file", "extension", "file format", "Excel Open XML", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"A fájlformátum útmutatója, hogy megtudja, mi az XLTX fájl és API-k, amelyek létrehozhatják és megnyithatják azokat.",
  "title" :"What is an XLTX file?",
  "linktitle" : "XLTX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Mi az XLTX fájl?

Az .xltx kiterjesztésű fájlok olyan Microsoft Excel-sablonfájlokat képviselnek, amelyek az Office OpenXML fájlformátum-specifikációin alapulnak. Egy szabványos sablonfájl létrehozására szolgál, amely felhasználható [XLSX](/hu/spreadsheet/xlsx/) fájlok létrehozására, amelyek az XLTX fájlban megadott beállításokkal megegyeznek.

## Rövid története

2000 elején a Microsoft a változtatás mellett döntött, hogy megfeleljen az **Office Open XML** szabványnak. Az új szabvány szerinti különböző típusú dokumentumokat úgy azonosították, hogy "X"-et fűztek a kiterjesztéseikhez, ahol az "X" az XML-t jelenti. 2007-re ez az új fájlformátum az Office 2007 részévé vált, és a Microsoft Office új verzióiban is érvényesül. Az új fájltípus további előnyökkel jár a kis fájlméret, a kisebb sérülések és a jól formázott képek megjelenítése miatt.

## XLTX fájlformátum specifikációi

Az XLTX fájlok az Office OpenXML fájlformátumon alapulnak, és XML és [ZIP](/hu/compression/zip/) használatával csökkentik a fájlméretet. A Microsoft Office 2007 kiadásával készült, hogy felváltsa a bináris XLT fájlformátumot. Az XLTX-hez hasonlóan az XLT fájlformátum is használható [XLS](/hu/spreadsheet/xls/) fájlok létrehozására a Microsoft Excel 2003 és 2007 használatával. Ezeket a Microsoft Excel programmal a fájlra dupla kattintással lehet megnyitni. A fájlok XLTX fájlformátumú szerveződése megfigyelhető, ha átnevezi a fájlt ZIP-re, majd kicsomagolja a tartalmát a lemezre.

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

* [[MS-XLSX] – .Xlsx fájlformátum](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

