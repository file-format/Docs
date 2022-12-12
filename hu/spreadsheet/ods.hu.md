{
  "date" : "2019-12-10",
  "keywords" :[ "ODS", "file", "extension", "file format", "OpenDocument Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"A fájlformátum útmutatója, hogy megtudja, mi az az ODS-fájl és az API-k, amelyek létrehozhatják és megnyithatják azokat.",
  "title" :"Mi az ODS-fájl?",
  "linktitle" : "ODS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Mi az ODS fájl?

Az .ods kiterjesztésű fájlok az OpenDocument Spreadsheet Document formátumot jelentik, amelyeket a felhasználó szerkeszthet. Az adatok az ODF fájlban sorokba és oszlopokba kerülnek. Ez XML-alapú formátum, és egyike az Open Document Formats (ODF) család számos altípusának. A formátumot az OASIS által közzétett és karbantartott ODF 1.2 specifikáció részeként határozták meg. Számos Windows-alkalmazás, valamint más operációs rendszerek képesek ODS-fájlok megnyitására szerkesztésre és manipulációra, beleértve a Microsoft Excelt, a NeoOffice-ot és a LibreOffice-ot. Az ODS-fájlok más táblázatformátumokba, például [XLS](/hu/spreadsheet/xls/), [XLSX](/hu/spreadsheet/xlsx/) és más formátumokba is konvertálhatók különböző alkalmazásokkal.

## Rövid története ##

Az ODS fájlformátum specifikációi az ODF specifikációként kifejlesztett szabványon alapulnak. Ezek a specifikációk az elmúlt időszakban az OASIS által kifejlesztett és közzétett három változat formájában fejlődtek, az alábbiak szerint:

"2005" - Az 1.0-s verzió 2005 májusában jelent meg

"2007" - Az 1.1-es verzió 2007 februárjában jelent meg

`2011` – Az 1.2-es verzió 2011 szeptemberében jelent meg

Elég apró változások történtek az ODF 1.0-ról az 1.1-es verziókra való áttéréskor. Az [ODF 1.2-es verzió] (https://www.oasis-open.org/standards#opendocumentv1.2) az ODF-specifikációk legújabb verziója, és a fejlesztőknek konzultálniuk kell vele az ODS-olvasáshoz/íráshoz kapcsolódó alkalmazások fejlesztésekor.

## ODS fájlformátum ##

Az OpenDocument formátum támogatja a dokumentumok egyetlen XML-dokumentumként történő megjelenítését, valamint több aldokumentum gyűjteményét egy csomagon belül [ZIP](/hu/compression/zip/) archívumként. A ZIP archívumból származó fájlok mindegyike a teljes dokumentum egy részét tárolja. Minden aldokumentum a dokumentum egy bizonyos aspektusát tárolja. Például egy aldokumentum tartalmazza a stílusinformációkat, egy másik pedig a dokumentum tartalmát. Egy tipikus ODF dokumentum a következő összetevőket tartalmazza:

* `content.xml` – Dokumentumtartalom és a tartalomban használt automatikus stílusok.
* `styles.xml` – A dokumentumtartalomban használt stílusok és magukban a stílusokban használt automatikus stílusok.
* `meta.xml` – A dokumentum metainformációi, például a szerző vagy az utolsó mentési művelet ideje.
* `settings.xml` – Alkalmazás-specifikus beállítások, például az ablak mérete vagy a nyomtató információi.

Ezeken kívül sok más aldokumentum is lehet a csomagban, mint például a dokumentum bélyegképe, képek stb.

A táblázatos dokumentumfájlok az ODF-fájlok azon részhalmaza, ahol a tartalom (lapok) a content.xml aldokumentumban tárolódnak.

## Referenciák ##

* [OpenDocument – Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

