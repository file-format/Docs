{
  "date" : "2019-12-10",
  "keywords" :[ "XLSX", "file", "extension", "file format", "Excel", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tudjon meg többet az XLSX fájlokról és az API-król, amelyek XLSX fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"XLSX fájlformátum - Mi az XLSX fájl?",
  "linktitle" : "XLSX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Mi az XLSX fájl?

Az **XLSX** a Microsoft Excel dokumentumok jól ismert formátuma, amelyet a Microsoft a Microsoft Office 2007 kiadásával vezetett be. A [2. részben] ismertetett nyílt csomagolási egyezmények szerint szervezett struktúra alapján (https://www. .ecma-international.org/publications/standards/Ecma-376.htm) az ECMA-376 OOXML-szabvány, az új formátum egy zip-csomag, amely számos XML-fájlt tartalmaz. Az alapul szolgáló struktúra és fájlok az .xlsx fájl egyszerű kicsomagolásával vizsgálhatók.

## Az XLSX fájlformátum rövid története

Az XLSX fájlformátumot 2007-ben vezették be, és a Microsoft által 2000-ben adaptált Open XML szabványt használja. Az XLSX előtt az [XLS](/hu/spreadsheet/xls/) általánosan használt fájlformátum volt, amely tiszta bináris fájlformátum volt. Az új fájltípus további előnyökkel jár: kis fájlméret, kevesebb sérülési változás és jól formázott képmegjelenítés. 2000 elején a Microsoft a változtatás mellett döntött, hogy megfeleljen az **Office Open XML** szabványnak. 2007-re ez az új fájlformátum az Office 2007 részévé vált, és a Microsoft Office új verzióiban is érvényesül.

## XLSX fájlformátum specifikációi

A hivatalos [XLSX fájlformátum-specifikáció](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e) online elérhető a Microsofttól. Az XLSX-fájl tartalmának megtekintéséhez nevezze át [ZIP](/hu/compression/zip/) fájlra a kiterjesztésének megváltoztatásával, majd bontsa ki az Excel-munkafüzet alkotófájljainak megtekintéséhez. Egy üres munkafüzet fájljaiba kicsomagolva a következő fájlokat és mappákat tartalmazza.

### [Content_Types].xml ###

Ez az egyetlen fájl, amely az alapszinten található a zip kicsomagolásakor. Felsorolja a csomagon belüli részek tartalomtípusait. Ebben az XML-fájlban minden, a csomagban található XML-fájlra való hivatkozás hivatkozik.

### \_rels (mappa) ###

Ez a Relationships mappa, amely egyetlen XML-fájlt tartalmaz, amely a csomagszintű kapcsolatokat tárolja. Az Xlsx fájlok kulcsfontosságú részeire mutató hivatkozásokat ez a fájl URI-ként tartalmazza. Ezek az URI-k azonosítják az egyes kulcselemek kapcsolatának típusát a csomaggal. Ez magában foglalja az xl/workbook.xml néven található elsődleges irodai dokumentumhoz és a docProps egyéb részeihez való viszonyt, mint alapvető és kiterjesztett tulajdonságokat.

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

## XLSX formátum példa ##


A munkafüzetben található minden Excel-munkalaphoz egy XML-fájl tartozik. Ezeket az XML fájlokat az xl/worksheets mappában találja. A munkalapon található összes információ az XML-fájl különböző szakaszaiba van rendezve. Vizsgáljuk meg a munkafüzet egy minta munkalapját, amely a következő képen látható.

{{< figure src="../XLSX file format.png" alt="XLSX fájlformátum" >}}

Amint látható, ez a munkalap az A1–B2 cellák tartalmát és egy képet tartalmaz. Ezenkívül a G13 cella jelenleg az aktív cella a munkalapon. Most vizsgáljuk meg az xl/worksheets/sheet1.xml fájlt, hogy megtudjuk, hogyan jelennek meg ezek az információk az XML fájlban. Ennek az XML-fájlnak a tartalma az alábbiak szerint látható.

{{< figure src="../XLSX File Format Details.png" alt="XPS fájlformátum" >}}

1. A lapon témaszín van alkalmazva. Az XML-fájlban szerepel a címkével<tabColor> a téma azonosítóját követve.
1. A Selected lap értéke 1, ami azt mutatja, hogy ez a kiválasztott lap
1. Ahogy a fenti első képen látható, a munkalap G13 cellája egy aktív cella, amely az XML fájlban is szerepel.
1. A sheetData fül a munkalapon található adatokat jeleníti meg. Látható azonban, hogy a munkalap eredeti tartalma sehol sem szerepel ebben a részben. Ennek az az oka, hogy a szöveg közvetett módon a "sharedStrings" XML-lapról hivatkozik. Ez a hivatkozás biztosítja, hogy minden szöveg csak egyszer kerüljön mentésre, és helytakarékosság érdekében újra hivatkozhasson rájuk.
1. A látható képre az "rId2" hivatkozási azonosító hivatkozik

## Hozzájárul

Meg kell osztania valamit az XLSX vagy a Spreadsheet fájlformátumokról? Megállapításait a [Spreadsheet File Format News](https://news.fileformat.com/t/Spreadsheet) részben teheti közzé.

## Hivatkozások

* [[MS-XLSX] - XLSX fájlformátum](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

