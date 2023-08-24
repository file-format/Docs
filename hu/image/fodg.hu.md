{
  "date" : "2019-10-11",
  "keywords" :[ "fodg fájl", "fodg fájlformátum", "mi az a fodg fájl", "fájl", "fodg példa", "fodg fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FODG - OpenDocument rajzfájl formátum",
  "description":"További információ a FODG fájlformátumról és az API-król, amelyek FODG fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "FODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a FODG fájl?

A .fodg kiterjesztésű fájl egy Apache OpenOffice Drawing fájlformátum rajzelemek tárolására. Az Advancement of Structural Information Standards (OASIS) által felvázolt fájlformátum-specifikációkon alapul. Egy másik hasonló fájlformátum az OpenOffice grafikákhoz az [ODG](/hu/image/odg/), amely vektorképként tárolja a rajzelemeket. A FODG fájlok OpenOffice és LibreOffice segítségével is megnyithatók. Az OpenOffice által támogatott egyéb fájlformátumok például az [ODT](/hu/word-processing/odt/), az ODF, az [ODP](/hu/presentation/odp/) és az [ODS](/hu/spreadsheet/ods/).

## FODG fájlformátum

A FODG az OpenDocument XML fájlformátumán alapul, amely megfelel az OASIS OpenDocument Format ISO/IEC 26300 szabványnak. Internet Media Type application/vnd.oasis.opendocument.graphics, valamint az org.oasis-open.opendocument public.composite-content szabványnak is megfelel. . Az XML-struktúra közös minden dokumentumtípusnál, például táblázatoknál, rajzfájloknál és szöveges dokumentumoknál. Az OpenOffice-dokumentumok a tartalom, a stílusok, a metaadatok és az alkalmazásbeállítások négy különálló XML-fájlba történő szétválasztásával kihasználják a problémák szétválasztását.

`<office:document-content>` - Dokumentumtartalom és a tartalomban használt automatikus stílusok.
`<office:document-styles>` - A dokumentumtartalomban használt stílusok és magukban a stílusokban használt automatikus stílusok.
`<office:document-meta>` - A dokumentum metainformációi, például a szerző vagy az utolsó mentési művelet ideje.
`<office:document-settings>` - Alkalmazás-specifikus beállítások, például az ablak mérete vagy a nyomtató információi.

## Referenciák ##
* [Az 1.3-as verzió szabványosításának jövőbeli specifikációi ](https://docs.oasis-open.org/office/OpenDocument/v1.3/cs01/OpenDocument-v1.3-cs01.zip)
* [OASIS Open Document Format for Office Applications](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [OpenDocument Format – Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

