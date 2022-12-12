{
  "date" : "2019-12-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"A fájlformátum útmutatója, hogy megtudja, mi az _XLSX fájl és API-k, amelyek létrehozhatnak és megnyithatnak _XLSX fájlokat.",
  "title" :"What is an _XLSX file?",
  "linktitle" : "_XLSX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-11-22"
}

## Mi az _XLSX fájl?

A .\_xlsx kiterjesztésű fájl valójában egy [XLSX](/hu/spreadsheet/xlsx/) fájl, amelyet egy másik alkalmazás nevez át. Ez megtörténhet bizonyos esetekben, amikor a fájlnév tartalmaz egy . a fájlnév végén. A \_XLSX fájlok az XLSX fájlokhoz hasonlóan megnyithatók a Microsoft Excel programban, ha ismét átnevezi őket .xlsx kiterjesztésre.

## _XLSX fájlformátum - További információ

Az _XLSX fájlok nem különböznek az XLSX fájloktól, és a Microsoft által 2000-ben elfogadott Open XML szabványt használják. Az XLSX előtt az [XLS](/hu/spreadsheet/xls/) volt az elsődleges fájlformátum, amelyet az Excel-táblázatokkal való munka során használtak dokumentumok mentésére. bináris formátumban. Ez az új XML-alapú fájlformátum olyan előnyökkel járt, mint a kis fájlméret, a fájlsérülésekkel szembeni ellenállás és a jól formázott képek megjelenítése. Ez az új XML alapú fájlformátum az Office 2007 részévé vált, és a Microsoft új verzióiban is megvalósul.

## \_XLSX fájlformátum specifikációi

Mivel a \_XLSX fájl egy átnevezett XLSX fájl, ugyanazokkal a specifikációkkal rendelkezik, mint az eredeti fájl. Ez csak egy archív fájl, amely a [ZIP](/hu/compression/zip/) archív fájlformátumon alapul. Ha meg szeretné tekinteni ennek az archívumnak a tartalmát, egyszerűen nevezze át a fájlt .zip kiterjesztésre, és bontsa ki az Excel-munkafüzet alkotófájljainak megtekintéséhez. Egy üres munkafüzet fájljaiba kicsomagolva a következő fájlokat és mappákat tartalmazza.

### [Content_Types].xml

Ez az egyetlen fájl, amely az alapszinten található a zip kicsomagolásakor. Felsorolja a csomagon belüli részek tartalomtípusait. Ebben az XML-fájlban minden, a csomagban található XML-fájlra való hivatkozás hivatkozik.

### \_rels (mappa)

Ez a Relationships mappa, amely egyetlen XML-fájlt tartalmaz, amely a csomagszintű kapcsolatokat tárolja. Az Xlsx fájlok kulcsfontosságú részeire mutató hivatkozásokat ez a fájl URI-ként tartalmazza. Ezek az URI-k azonosítják az egyes kulcselemek kapcsolatának típusát a csomaggal. Ez magában foglalja az xl/workbook.xml néven található elsődleges irodai dokumentumhoz és a docProps egyéb részeihez való viszonyt, mint alapvető és kiterjesztett tulajdonságokat.

### docProps

Ez a mappa tartalmazza a dokumentum általános tulajdonságait. Ezek közé tartozik az alapvető tulajdonságok készlete, a kiterjesztett vagy alkalmazásspecifikus tulajdonságok készlete, valamint a dokumentum miniatűr előnézete. Egy üres munkafüzet két fájlt tartalmaz ebben a mappában: app.xml és core.xml. A core.xml olyan információkat tartalmaz, mint a szerző, a létrehozás és mentés dátuma, valamint a módosítás. Az App.xml információkat tartalmaz a fájl tartalmáról.

### xl (mappa)

Ez a fő mappa, amely a munkafüzet tartalmával kapcsolatos összes részletet tartalmazza. Alapértelmezés szerint a következő mappákkal rendelkezik:

* \_rels
* téma
* munkalapok

és a következő xml fájlok:

* styles.xml
* munkafüzet.xml

## Hivatkozások

* [MS-XLSX - .xlsx fájlformátum](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

