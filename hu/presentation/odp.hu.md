{
  "date" : "2019-10-11",
  "keywords" :[ "odp fájl", "odp fájlformátum", "mi az odp fájl", "fájl", "odp példa", "odp fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ODP - OpenOffice prezentációs fájlformátum",
  "description":"További információ az ODP fájlformátumról és az API-król, amelyek ODP-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "ODP",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az ODP fájl?

Az .odp kiterjesztésű fájlok az OpenOffice.org által az OASISOpen szabványban használt prezentációs fájlformátumot képviselik. A prezentációs fájl olyan diák gyűjteménye, amelyben minden diák szöveget, képeket, formázást, animációt és egyéb médiát tartalmazhat. Ezeket a diákat egyéni prezentációs beállításokkal rendelkező diavetítések formájában mutatják be a közönségnek. Az ODP-fájlokat olyan alkalmazások nyithatják meg, amelyek megfelelnek az OpenDocument formátumnak (például OpenOffice vagy StarOffice).

## Rövid története

Az ODP fájlformátum specifikációi az ODF specifikációként kifejlesztett szabványon alapulnak. Ezek a specifikációk az elmúlt időszakban az OASIS által kifejlesztett és közzétett három változat formájában fejlődtek, az alábbiak szerint:

"2005" - Az 1.0-s verzió 2005 májusában jelent meg
"2007" - Az 1.1-es verzió 2007 februárjában jelent meg
`2011` – Az 1.2-es verzió 2011 szeptemberében jelent meg

Elég apró változások történtek az ODF 1.0-ról az 1.1-es verziókra való áttéréskor. Az [ODF 1.2-es verzió](https://www.oasis-open.org/standards#opendocumentv1.2) az ODF-specifikációk legújabb verziója, és a fejlesztőknek konzultálniuk kell vele az ODS-olvasáshoz/íráshoz kapcsolódó alkalmazások fejlesztésekor.

## A fájlformátum specifikációi

Az OpenDocument formátum támogatja a dokumentumok egyetlen XML-dokumentumként való megjelenítését, valamint egy csomagon belüli több aldokumentum gyűjteményét [ZIP](https://docs.fileformat.com/compression/zip/) archívumként. A ZIP archívumból származó fájlok mindegyike a teljes dokumentum egy részét tárolja. Minden aldokumentum a dokumentum egy bizonyos aspektusát tárolja. Például egy aldokumentum tartalmazza a stílusinformációkat, egy másik pedig a dokumentum tartalmát. Egy tipikus ODF dokumentum a következő összetevőket tartalmazza:

* `content.xml` – Dokumentumtartalom és a tartalomban használt automatikus stílusok.
* `styles.xml` – A dokumentumtartalomban használt stílusok és magukban a stílusokban használt automatikus stílusok.
* `meta.xml` – A dokumentum metainformációi, például a szerző vagy az utolsó mentési művelet ideje.
* `settings.xml` – Alkalmazás-specifikus beállítások, például az ablak mérete vagy a nyomtató információi.

Ezeken kívül sok más aldokumentum is lehet a csomagban, mint például a dokumentum bélyegképe, képek stb.

A táblázatos dokumentumfájlok az ODF-fájlok azon részhalmaza, ahol a tartalom (lapok) a content.xml aldokumentumban tárolódnak.

## Hivatkozások

* [OpenDocument – Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

